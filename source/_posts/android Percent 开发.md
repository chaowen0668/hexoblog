title: android Percent开发   
date: 2015-09-02 12:50:29  
categories: android

---
Android的布局支持百分比的设置进行开发，来学习如何去实现它，不过看起来会像网页的设置，比如宽度的设置属性是`layout_widthPercent`。在此之前，我们一般都会设置Linearlayout的weight权重来实现布局间的比例大小。
<!--more-->

Percent support Library提供了两个新的类:  

1. PercentRelativeLayout
2. PercentFrameLayout

# 创建新项目 #

创建一个新的项目来测试，修改`build.gradle`,需要引入以下库
apply plugin: 'com.android.application'

	android {
	    compileSdkVersion 23
	    buildToolsVersion "23.0.0"
	
	    defaultConfig {
	        applicationId "com.android.chaowen.percentdemo1"
	        minSdkVersion 7
	        targetSdkVersion 22
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
	    compile 'com.android.support:support-annotations:23.0.0'
	    compile 'com.android.support:appcompat-v7:23.0.0'
	    compile 'com.android.support:design:23.0.0'
	    compile 'com.android.support:percent:23.0.0'
	}

# 创建布局 #
	
	<android.support.percent.PercentRelativeLayout 
	  xmlns:android="http://schemas.android.com/apk/res/android"
	  xmlns:app="http://schemas.android.com/apk/res-auto"
	  xmlns:tools="http://schemas.android.com/tools"
	  android:layout_width="match_parent"
	  android:layout_height="match_parent"
	  tools:context=".MainActivity">
	
	  <View
	    android:id="@+id/first"
	    android:background="@color/sa_green_dark"
	    app:layout_heightPercent="50%"
	    app:layout_marginLeftPercent="25%"
	    app:layout_marginTopPercent="25%"
	    app:layout_widthPercent="50%" />
	
	  <View
	    android:layout_width="0dp"
	    android:layout_height="32dp"
	    android:layout_alignLeft="@id/first"
	    android:layout_alignStart="@id/first"
	    android:layout_alignRight="@id/first"
	    android:layout_alignEnd="@id/first"
	    android:layout_below="@id/first"
	    android:layout_marginTop="8dp"
	    android:background="@color/light_grey" />
	  
	</android.support.percent.PercentRelativeLayout>


  比例大小是通过`heightPercent`和`widthPercent`属性来设置百分比大小值。完全属于`RelativeLayout`的扩展类，值得一提的是，
不再需要设置`layout_width`和`layout_height`，注意了，这是新的库使用方法，因为这两个属性会被自动加入了。

百度比也可以用于设置边距。唯一区别的只是采取了百分比值。

最后一点需要注意，在第二个view，并没有直接设置比例的大小，但是它的位置是相对于第一个view.