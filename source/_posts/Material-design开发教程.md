title: Material design开发教程
date: 2015-10-11 10:53:52
tags: android
categories: android

---
本课程学习使用Material Design开发

# 使用Android studio创建一个Material Design项目 #
Material Design的效果是Android5.0 Lollipop才有的效果，要兼容到5.0以下的Android，需要使用AppCompatv21的开发包。本文将演示如何创建一个Material Design的应用。

## 添加AppCompat依赖包 ##
在项目的build.gradle文件中，添加appCompart包，我使用的是23.0.1的版本，根据你的本机开发环境对应的版本修改即可。
```
apply plugin: 'com.android.application'

android {
    compileSdkVersion 23
    buildToolsVersion "23.0.1"

    defaultConfig {
        applicationId "com.chaowen.materialdemo"
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
}

dependencies {
    compile fileTree(dir: 'libs', include: ['*.jar'])
    compile 'com.android.support:appcompat-v7:23.0.1'
}
```

## 指定Material Design主题 ##
将自己的主题继承自Theme.AppCompat，新的AppCompat有你所需要的支持Material Design的兼容代码与资源文件。
```
<resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="AppTheme.Base">
    </style>
    <style name="AppTheme.Base" parent="Theme.AppCompat">
     
    </style>
</resources>
```

如果没有values-v21的文件夹，需要创建一个values-v21的文件夹，并创建一个styles.xml文件。
继承AppTheme.Base主题即可。
```
<resources>

    <style name="AppTheme" parent="AppTheme.Base">
      
    </style>

</resources>
```
以上就是创建Material Design的项目过程。

# 使用Material Design Color指定色调 #
先来认识几个重要的属性
colorPrimary 对应ActionBar的颜色。
colorPrimaryDark对应状态栏的颜色
colorAccent 对应EditText编辑时、RadioButton选中、CheckBox等选中时的颜色。

![](http://images.cnitblog.com/blog/651487/201411/071629282842265.png)

打开values下的styles.xml文件，添加以下3个属性
```
<resources>

    <!-- Base application theme. -->
    <style name="AppTheme" parent="AppTheme.Base">
    </style>
    <style name="AppTheme.Base" parent="Theme.AppCompat.Light">
        <item name="colorPrimary">#2196F3</item>
        <item name="colorPrimaryDark">#0D47A1</item>
        <item name="colorAccent">#E91E63</item>
    </style>
</resources>
```

我们还需要在vlues-v21中的styles.xml文件中作些修改
```
<resources>

    <style name="AppTheme" parent="AppTheme.Base">
        <item name="android:colorPrimary">#2196F3</item>
        <item name="android:colorPrimaryDark">#0D47A1</item>
        <item name="android:colorAccent">#E91E63</item>
    </style>

</resources>
```
两者之间的区别是colorPrimary与android:colorPrimary。因为android:colorPrimary仅仅只能在android 5.0或者以上的设备中使用，但是AppCompat中提供的colorPrimary却不是。

