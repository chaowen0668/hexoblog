title: LayoutAnimation动画使用
date: 2015-09-17 17:22:05
tags: 动画
categories: android

---
在Android中，最简单的动画就是补间动画了。通过补间动画，可以对一个控件进行位移、缩放、旋转、改变透明度等动画。但是补间动画只能对一个控件使用，如果要对某一组控件播放一样的动画的话，可以考虑layout-animation。
<!--more-->

# 两种实现方式 #
1. xml实现
2. 代码实现

# xml实现方式 #
由于layout-animation是对于某一组控件的操作，就需要一个基本的动画来定义单个控件的动画。另外还可以定义动画的显示顺序和延迟：  
1. 在anim目录下新建一个`list_anim_layout.xml`文件

```
<?xml version="1.0" encoding="utf-8"?>
<layoutAnimation xmlns:android="http://schemas.android.com/apk/res/android"
    android:delay="30%"
    android:animationOrder="reverse"
    android:animation="@anim/slide_right" />
```
`android:delay`表示动画播放的延时，既可以是百分比，也可以是float小数。
`android:animationOrder`表示动画的播放顺序，有三个取值normal(顺序)、reverse(反序)、random(随机)。
`android:animation`指向了子控件所要播放的动画。

 2.继续在anim目录下新建文件slide_right.xml文件

```
<?xml version="1.0" encoding="utf-8"?>
<set xmlns:android="http://schemas.android.com/apk/res/android"
    android:interpolator="@android:anim/accelerate_interpolator">
    <translate android:fromXDelta="-100%p" android:toXDelta="0"
        android:duration="@android:integer/config_shortAnimTime" />
</set>
```

3.上述步骤完成之后，就可以将layout-animation应用到ViewGroup中，xml布局添加下面一行就ok： 
```
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent"
    android:layout_height="match_parent" android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingBottom="@dimen/activity_vertical_margin" tools:context=".MainActivity">

    <ListView
        android:id="@+id/lv"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layoutAnimation="@anim/list_anim_layout"></ListView>

</RelativeLayout>
```

# 代码实现 #
```
        Animation animation= AnimationUtils.loadAnimation(this, R.anim.slide_right);
        //得到一个LayoutAnimationController对象；
        LayoutAnimationController lac=new LayoutAnimationController(animation);
        //设置控件显示的顺序；
        lac.setOrder(LayoutAnimationController.ORDER_REVERSE);
        //设置控件显示间隔时间；
        lac.setDelay(1);
        //为ListView设置LayoutAnimationController属性；
        lv.setLayoutAnimation(lac);
        lv.startLayoutAnimation();
```
