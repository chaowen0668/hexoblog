title: Rxjava学习教程
date: 2015-10-15 17:14:23
tags: Rxjava
categories: java

---
# RxJava与众不同之处 #
从纯Java的观点看，RxJava Observable类源自于经典的Gang Of Four的观察者模式。

它添加了三个缺少的功能：

- 生产者在没有更多数据可用时能够发出信号通知：onCompleted()事件。
- 生产者在发生错误时能够发出信号通知：onError()事件。
- RxJava Observables 能够组合而不是嵌套，从而避免开发者陷入回调地狱。

# 四种角色 #
- Observable
- Observer
- Subscriber
- Subjects
Observables和Subjects是两个"生产"实体,Observers和Subscribers是两个"消费"实体

# 概念 #
RxJava 有四个基本概念：`Observable` (可观察者，即被观察者)、 `Observer` (观察者)、 `subscribe` (订阅)、事件。`Observable` 和 `Observer` 通过 `subscribe() `方法实现订阅关系，从而 Observable 可以在需要的时候发出事件来通知 `Observer`

<!--more-->

与传统观察者模式不同， RxJava 的事件回调方法除了普通事件 onNext() （相当于 onClick() / onEvent()）之外，还定义了两个特殊的事件：`onCompleted()` 和 `onError()`

- onCompleted(): 事件队列完结。RxJava 不仅把每个事件单独处理，还会把它们看做一个队列。RxJava 规定，当不会再有新的 onNext() 发出时，需要触发 onCompleted() 方法作为标志。
- onError(): 事件队列异常。在事件处理过程中出异常时，onError() 会被触发，同时队列自动终止，不允许再有事件发出。
- 在一个正确运行的事件序列中, onCompleted() 和 onError() 有且只有一个，并且是事件序列中的最后一个。需要注意的是，onCompleted() 和 onError() 二者也是互斥的，即在队列中调用了其中一个，就不应该再调用另一个。

RxJava 的观察者模式大致如下图：

![](http://i.imgur.com/fer9igK.png)

# 基本实现 #

## 创建Observer ##
Observer 即观察者，它决定事件触发的时候将有怎样的行为。 RxJava 中的 Observer 接口的实现方式：
```
Observer<String> observer = new Observer<String>() {
    @Override
    public void onNext(String s) {
        Log.d(tag, "Item: " + s);
    }

    @Override
    public void onCompleted() {
        Log.d(tag, "Completed!");
    }

    @Override
    public void onError(Throwable e) {
        Log.d(tag, "Error!");
    }
};
```

除了 Observer 接口之外，RxJava 还内置了一个实现了 Observer 的抽象类：`Subscriber`。 `Subscriber` 对 `Observer` 接口进行了一些扩展，但他们的基本使用方式是完全一样的：
```
Subscriber<String> subscriber = new Subscriber<String>() {
    @Override
    public void onNext(String s) {
        Log.d(tag, "Item: " + s);
    }

    @Override
    public void onCompleted() {
        Log.d(tag, "Completed!");
    }

    @Override
    public void onError(Throwable e) {
        Log.d(tag, "Error!");
    }
};
```



1. `onStart()`: 这是 `Subscriber` 增加的方法。它会在 subscribe 刚开始，而事件还未发送之前被调用，可以用于做一些准备工作，例如数据的清零或重置。这是一个可选方法，默认情况下它的实现为空。需要注意的是，如果对准备工作的线程有要求（例如弹出一个显示进度的对话框，这必须在主线程执行）， `onStart()` 就不适用了，因为它总是在 `subscribe` 所发生的线程被调用，而不能指定线程。要在指定的线程来做准备工作，可以使用 `doOnSubscribe()` 方法，具体可以在后面的文中看到。
2. `unsubscribe()`: 这是 `Subscriber` 所实现的另一个接口 `Subscription` 的方法，用于取消订阅。在这个方法被调用后，`Subscriber` 将不再接收事件。一般在这个方法调用前，可以使用 `isUnsubscribed()` 先判断一下状态。 `unsubscribe()` 这个方法很重要，因为在 `subscribe()` 之后， `Observable` 会持有 `Subscriber` 的引用，这个引用如果不能及时被释放，将有内存泄露的风险。所以最好保持一个原则：要在不再使用的时候尽快在合适的地方（例如 `onPause()` `onStop()` 等方法中）调用 `unsubscribe()` 来解除引用关系，以避免内存泄露的发生。

## 创建 Observable ##
Observable 即被观察者，它决定什么时候触发事件以及触发怎样的事件。 RxJava 使用 create() 方法来创建一个 Observable ，并为它定义事件触发规则：
```
Observable observable = Observable.create(new Observable.OnSubscribe<String>() {
    @Override
    public void call(Subscriber<? super String> subscriber) {
        subscriber.onNext("Hello");
        subscriber.onNext("Hi");
        subscriber.onNext("Aloha");
        subscriber.onCompleted();
    }
});
```
以看到，这里传入了一个 OnSubscribe 对象作为参数。OnSubscribe 会被存储在返回的 Observable 对象中，它的作用相当于一个计划表，当 Observable 被订阅的时候，OnSubscribe 的 call() 方法会自动被调用，事件序列就会依照设定依次触发（对于上面的代码，就是观察者Subscriber 将会被调用三次 onNext() 和一次 onCompleted()）。这样，由被观察者调用了观察者的回调方法，就实现了由被观察者向观察者的事件传递，即观察者模式。

## Subscribe (订阅) ##
创建了 Observable 和 Observer 之后，再用 subscribe() 方法将它们联结起来，整条链子就可以工作了。代码形式很简单：
```
observable.subscribe(observer);
// 或者：
observable.subscribe(subscriber);
```

有人可能会注意到， subscribe() 这个方法有点怪：它看起来是『observalbe 订阅了 observer / subscriber』而不是『observer / subscriber 订阅了 observalbe』，这看起来就像『杂志订阅了读者』一样颠倒了对象关系。这让人读起来有点别扭，不过如果把 API 设计成 observer.subscribe(observable) / subscriber.subscribe(observable) ，虽然更加符合思维逻辑，但对流式 API 的设计就造成影响了，比较起来明显是得不偿失的。

# Android 中使用Lambda表达式 #
Android Studio默认使用Lambda表达式是会报错的，即使你使用的是java 8，为了在android studio中使用lambda表达式，我们必须借助一个插件retrolambda ，该插件将java 8中的lambda表达式特性兼容到java 5。使用它也很简单。



首先先项目根目录下的build.gradle中加入

   `classpath 'me.tatarka:gradle-retrolambda:3.2.0'`

最终整个文件会像这样子
```
buildscript {
    repositories {
        jcenter()
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:1.2.3'
        classpath 'me.tatarka:gradle-retrolambda:3.2.0'
    }
}

allprojects {
    repositories {
        jcenter()
    }
}
```

然后再module目录下的build.gradle中使用插件，加入

    apply plugin: 'me.tatarka.retrolambda'

并且在android节点下加入
```
compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
```

# 基本使用 #
## 创建 Observer ##
Observer 即观察者，它决定事件触发的时候将有怎样的行为。 RxJava 中的 Observer 接口的实现方式：

```
/**
     * 创建观察者
     */
    Observer<String> observer = new Observer<String>() {
        @Override
        public void onCompleted() {
            Log.d("observer","onCompleted ");
        }

        @Override
        public void onError(Throwable e) {
            Log.d("observer","error ");
        }

        @Override
        public void onNext(String s) {
             Log.d("observer","Item: " + s);
        }
    };
```

除了 Observer 接口之外，RxJava 还内置了一个实现了 Observer 的抽象类：`Subscriber`。 Subscriber 对 Observer 接口进行了一些扩展，但他们的基本使用方式是完全一样的：
```
Subscriber<String> subscriber = new Subscriber<String>() {
    @Override
    public void onNext(String s) {
        Log.d(tag, "Item: " + s);
    }

    @Override
    public void onCompleted() {
        Log.d(tag, "Completed!");
    }

    @Override
    public void onError(Throwable e) {
        Log.d(tag, "Error!");
    }
};
```
不仅基本使用方式一样，实质上，在 RxJava 的 subscribe 过程中，Observer 也总是会先被转换成一个 Subscriber 再使用。所以如果你只想使用基本功能，选择 Observer 和 Subscriber 是完全一样的。它们的区别对于使用者来说主要有两点：

`onStart()`: 这是 Subscriber 增加的方法。它会在 subscribe 刚开始，而事件还未发送之前被调用，可以用于做一些准备工作，例如数据的清零或重置。这是一个可选方法，默认情况下它的实现为空。需要注意的是，如果对准备工作的线程有要求（例如弹出一个显示进度的对话框，这必须在主线程执行）， onStart() 就不适用了，因为它总是在 subscribe 所发生的线程被调用，而不能指定线程。要在指定的线程来做准备工作，可以使用 doOnSubscribe() 方法，具体可以在后面的文中看到。
`unsubscribe()`: 这是 Subscriber 所实现的另一个接口 Subscription 的方法，用于取消订阅。在这个方法被调用后，Subscriber 将不再接收事件。一般在这个方法调用前，可以使用 isUnsubscribed() 先判断一下状态。 unsubscribe() 这个方法很重要，因为在 subscribe() 之后， Observable 会持有 Subscriber 的引用，这个引用如果不能及时被释放，将有内存泄露的风险。所以最好保持一个原则：要在不再使用的时候尽快在合适的地方（例如 onPause() onStop() 等方法中）调用 unsubscribe() 来解除引用关系，以避免内存泄露的发生。

## 创建 Observable ##
Observable 即被观察者，它决定什么时候触发事件以及触发怎样的事件。 RxJava 使用 create() 方法来创建一个 Observable ，并为它定义事件触发规则：
```
Observable observable = Observable.create(new Observable.OnSubscribe<String>() {
    @Override
    public void call(Subscriber<? super String> subscriber) {
        subscriber.onNext("Hello");
        subscriber.onNext("Hi");
        subscriber.onNext("Aloha");
        subscriber.onCompleted();
    }
});
```
可以看到，这里传入了一个 OnSubscribe 对象作为参数。OnSubscribe 会被存储在返回的 Observable 对象中，它的作用相当于一个计划表，当 Observable 被订阅的时候，OnSubscribe 的 call() 方法会自动被调用，事件序列就会依照设定依次触发（对于上面的代码，就是观察者Subscriber 将会被调用三次 onNext() 和一次 onCompleted()）。这样，由被观察者调用了观察者的回调方法，就实现了由被观察者向观察者的事件传递，即观察者模式。

## Subscribe (订阅) ##
创建了 Observable 和 Observer 之后，再用 subscribe() 方法将它们联结起来，整条链子就可以工作了。代码形式很简单：
```
observable.subscribe(observer);
// 或者：
observable.subscribe(subscriber);
```

## 简洁的写法 ##
### 简化Observable 使用just ###
`just(T...):`将传入的参数依次发送出来。
```
 Observable observable = Observable.just("Hello", "Hi", "Aloha");
```

### 简化Subscriber使用Action1类 ###

我们其实并不关心OnComplete和OnError，我们只需要在onNext的时候做一些处理，这时候就可以使用Action1类
```
Action1<String> onNextAction = new Action1<String>() {
        @Override
        public void call(String s) {
             System.out.println("action--"+s);
        }
    };
```
最终完整的代码
```
 Observable.just("Hello","chaowen")
                .subscribe(new Action1<String>() {
                    @Override
                    public void call(String s) {
                        System.out.println(s);
                    }
                });
```

### 使用java8的lambda可以使代码更简洁 ###
```
 Observable.just("Hello","chaowen")
                .subscribe(s -> System.out.println(s));
```

# 操作符 #
 操作符就是为了解决对Observable对象的变换的问题，操作符用于在Observable和最终的Subscriber之间修改Observable发出的事件。RxJava提供了很多很有用的操作符。

## map操作符的使用 ##
map操作符，就是用来把把一个事件转换为另一个事件的
以下代码演示如果在字符串新加字符
```
Observable.just("Hello chaowen")
                .map(new Func1<String, String>() {
                    @Override
                    public String call(String s) {
                        return s+"bifeng";
                    }
                })
                .subscribe(s -> System.out.println(s));
```
```
 Observable.just("Hello chaowen")
                .map(s -> s+"bifeng")
                .subscribe(s -> System.out.println(s));
```

map操作符更有趣的一点是它不必返回Observable对象返回的类型，你可以使用map操作符返回一个发出新的数据类型的observable对象。
```
Observable.just("Hello, world!")
    .map(new Func1<String, Integer>() {
        @Override
        public Integer call(String s) {
            return s.hashCode();
        }
    })
    .subscribe(i -> System.out.println(Integer.toString(i)));
```
简化代码

```
Observable.just("Hello, world!")  
    .map(s -> s.hashCode())  
    .subscribe(i -> System.out.println(Integer.toString(i)));
```


## zip数据合并操作 ##



# 第一个例子 #
RxAndroid的git地址： https://github.com/ReactiveX/RxAndroid

1.添加依赖
  ```
   compile 'io.reactivex:rxandroid:1.2.0'
   compile 'io.reactivex:rxjava:1.1.4'
   ```
2.在Android中使用Lambda表达式
   https://github.com/evant/gradle-retrolambda
   


1. 在项目的build.gradle文件中，加入

   ```
classpath 'me.tatarka:gradle-retrolambda:3.2.5'
```

2. 在app的module下加入以下代码
```
apply plugin: 'me.tatarka.retrolambda'

compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }

```
完整代码
```
apply plugin: 'com.android.application'
apply plugin: 'me.tatarka.retrolambda'
android {
    compileSdkVersion 23
    buildToolsVersion "23.0.1"

    defaultConfig {
        applicationId "com.example.chaowen.hellorxjava"
        minSdkVersion 15
        targetSdkVersion 23
        versionCode 1
        versionName "1.0"
    }
    buildTypes {
        release {
            minifyEnabled false
            proguardFiles getDefaultProguardFile('proguard-android.txt'), 'proguard-rules.pro'
        }
    }

    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}



dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile 'com.android.support:appcompat-v7:23.1.1'
    compile 'io.reactivex:rxandroid:1.2.0'
    compile 'io.reactivex:rxjava:1.1.4'
    compile 'com.jakewharton:butterknife:6.0.0'
    compile 'com.android.support:support-annotations:23.1.1'
}
```










https://github.com/lzyzsd/Awesome-RxJava
