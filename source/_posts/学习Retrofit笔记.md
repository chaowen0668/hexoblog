title: 学习Retrofit笔记
date: 2015-11-24 15:41:09
tags:
categories: android

---

本文是基于Retrofit2进行学习。首先你要知道Retrofit是一个网络请求框架，它的api 定义可以查阅[官网](http://square.github.io/retrofit/#api-declaration).
<!--more-->

# 从零开始搭建一个Retrofit的例子 #
以下示例会分别列出`Retrofit 1.9`和`Retrofit 2`的区别用法
## 添加依赖 ##

Retrofit 1.9

```
dependencies {  
    // Retrofit & OkHttp
    compile 'com.squareup.retrofit:retrofit:1.9.0'
    compile 'com.squareup.okhttp:okhttp:2.2.0'
}
```

Retrofit 2

```
dependencies {  
    // Retrofit & OkHttp
    compile 'com.squareup.retrofit:retrofit:2.0.0-beta2'
}
```

## Api服务核心类 ##
ServiceGenerator是项目的http核心类，专门用于封装http请求的基类。

Retrofit 1.9

```
public class ServiceGenerator {

    public static final String API_BASE_URL = "http://your.api-base.url";

    private static RestAdapter.Builder builder = new RestAdapter.Builder()
                .setEndpoint(API_BASE_URL)
                .setClient(new OkClient(new OkHttpClient()));

    public static <S> S createService(Class<S> serviceClass) {
        RestAdapter adapter = builder.build();
        return adapter.create(serviceClass);
    }
}
```

Retrofit 2

```
public class ServiceGenerator {
    public static final String API_BASE_URL = "http://api.github.com";

    private static OkHttpClient httpClient = new OkHttpClient();
    private static Retrofit.Builder builder =
            new Retrofit.Builder()
                    .baseUrl(API_BASE_URL)
                    .addConverterFactory(GsonConverterFactory.create());

    public static <S> S createService(Class<S> serviceClass) {
        Retrofit retrofit = builder.client(httpClient).build();
        return retrofit.create(serviceClass);
    }
}
```

## Json解析 ##
Retrofit 1.9默认带有Gson的支持。Retorfit2就需要自定义添加支持。

```
compile 'com.squareup.retrofit:converter-gson:2.0.0-beta2' 
``` 

## Api调用范例 ##
这里我会以github的API为例。

### 声明GitHubClient类 ###
Retrofit 1.9

```
public interface GitHubClient {  
    @GET("/repos/{owner}/{repo}/contributors")
    List<Contributor> contributors(
        @Path("owner") String owner,
        @Path("repo") String repo
    );
}
```

Retrofit 2

```
public interface GitHubClient {  
    @GET("/repos/{owner}/{repo}/contributors")
    Call<List<Contributor>> contributors(
        @Path("owner") String owner,
        @Path("repo") String repo
    );
}
```

### Model类 ###

```
class Contributor {  
    String login;
    int contributions;
}
```

### 请求 ###

Retrofit 1.9

```
    GitHubClient client = ServiceGenerator.createService(GitHubClient.class);

    // Fetch and print a list of the contributors to this library.
    List<Contributor> contributors =
        client.contributors("fs_opensource", "android-boilerplate");

    for (Contributor contributor : contributors) {
        System.out.println(
                contributor.login + " (" + contributor.contributions + ")");
    }
```

Retrofit 2

```
    GitHubClient client = ServiceGenerator.createService(GitHubClient.class);

        // Fetch and print a list of the contributors to this library.
        Call<List<Contributor>> call =
                client.contributors("lzyzsd", "Awesome-RxJava");

        List<Contributor> contributors = null;
        try {
            contributors = call.execute().body();
            for (Contributor contributor : contributors) {
                System.out.println(
                        contributor.login + " (" + contributor.contributions + ")");
            }
        } catch (IOException e) {
            e.printStackTrace();
        }
```

# 实现一个基本的登录 #
## 修改ServiceGenerator ##
修改ServiceGenerator类，添加一个新方法

Retrofit 1.9
```
public class ServiceGenerator {

    public static final String API_BASE_URL = "http://your.api-base.url";

    private static RestAdapter.Builder builder = new RestAdapter.Builder()
                .setEndpoint(API_BASE_URL)
                .setClient(new OkClient(new OkHttpClient()));

    public static <S> S createService(Class<S> serviceClass) {
        return createService(serviceClass, null, null);
    }

    public static <S> S createService(Class<S> serviceClass, String username, String password) {
        if (username != null && password != null) {
            // concatenate username and password with colon for authentication
            String credentials = username + ":" + password;
            // create Base64 encodet string
            final String basic =
                    "Basic " + Base64.encodeToString(credentials.getBytes(), Base64.NO_WRAP);

            builder.setRequestInterceptor(new RequestInterceptor() {
                @Override
                public void intercept(RequestFacade request) {
                    request.addHeader("Authorization", basic);
                    request.addHeader("Acceppt", "application/json");
                }
            });
        }

        RestAdapter adapter = builder.build();
        return adapter.create(serviceClass);
    }
}
```

Retrofit 2
```
public class ServiceGenerator {
    public static final String API_BASE_URL = "http://api.github.com";

    private static OkHttpClient httpClient = new OkHttpClient();
    private static Retrofit.Builder builder =
            new Retrofit.Builder()
                    .baseUrl(API_BASE_URL)
                    .addConverterFactory(GsonConverterFactory.create());

    public static <S> S createService(Class<S> serviceClass) {
        Retrofit retrofit = builder.client(httpClient).build();
        return retrofit.create(serviceClass);
    }

    public static <S> S createService(Class<S> serviceClass,String username,String password){
        if (username != null && password != null) {
            String credentials = username + ":" + password;
            final String basic =
                    "Basic " + Base64.encodeToString(credentials.getBytes(), Base64.NO_WRAP);

            httpClient.interceptors().clear();
            httpClient.interceptors().add(new Interceptor() {
                @Override
                public Response intercept(Interceptor.Chain chain) throws IOException {
                    Request original = chain.request();

                    Request.Builder requestBuilder = original.newBuilder()
                            .header("Authorization", basic)
                            .header("Accept", "applicaton/json")
                            .method(original.method(), original.body());

                    Request request = requestBuilder.build();
                    return chain.proceed(request);
                }
            });
        }

        Retrofit retrofit = builder.client(httpClient).build();
        return retrofit.create(serviceClass);

    }
}
```

## 添加LoginServer ##
Retrofit 1.9
```
public interface LoginService {  
    @POST("/login")
    User basicLogin();
}
```

Retrofit 2
```
public interface LoginService {  
    @POST("/login")
    Call<User> basicLogin();
}
```

## 调用示例 ##
Retrofit 1.9
```
LoginService loginService =  
    ServiceGenerator.createService(LoginService.class, "user", "secretpassword");
User user = loginService.basicLogin();  
```

Retrofit 2
```
LoginService loginService =  
   ServiceGeneratorcreateService(LoginService.class, "user", "secretpassword");
Call<User> call = loginService.basicLogin();  
User user = call.execute().body();  
```
