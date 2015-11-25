title: android开发技巧
date: 2015-09-08 13:06:26
tags:
categories: android

---
# UI技巧 #
[Drawable 着色的后向兼容方案](http://www.race604.com/tint-drawable/ )
[UI实时预览最佳实践](https://github.com/tianzhijiexian/Android-Best-Practices/blob/master/2015.9/ui/ui.md)
[Tinting drawables](http://andraskindler.com/blog/2015/tinting_drawables/?utm_source=androiddevdigest)
[Android 高清加载巨图方案 拒绝压缩图片](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1021/3607.html)
[Android ToolBar 的简单封装](http://blog.csdn.net/jxxfzgy/article/details/46476903)
[Android中Canvas绘图基础详解](http://blog.csdn.net/iispring/article/details/49770651)
[关于使用 CardView 开发过程中要注意的细节](http://blog.feng.moe/2015/10/24/something-about-cardview-development/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[实践自定UI](http://www.jianshu.com/p/11210b14f743)
[实践自定义UI2](http://www.jianshu.com/p/ff8dcefce371)
[自定义View的onMeasure、onLayout](http://yifeiyuan.me/2015/10/12/%E8%87%AA%E5%AE%9A%E4%B9%89View%E7%9A%84onMeasure%E3%80%81onLayout/)
[Android快捷方式解密](http://www.jianshu.com/p/dc3d04337d00)
[ViewPager不为人知的秘密](http://www.jianshu.com/p/80891d0185f7)
[Android Support Library 兼容库概念性介绍](http://zhuanlan.zhihu.com/zmywly8866/20260335)
[RecyclerView添加Header的正确方式](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1120/3705.html)



## 关于RadioButton setCheck方法的问题 ##
在做项目过程中，使用radioButton来做菜单切换导航，发现在RadioButton在与其他按钮来回切换会背景不生效,可以使用以下代码
```
rg.clearCheck();//清除选中状态的 
```

[参考来源](http://stackoverflow.com/questions/4035465/android-radiobutton-not-able-to-unset-using-setcheckedfalse-method)


# 代码优化 #
[ 利用 Android Annotations 来玩玩契约编程](http://blog.csdn.net/feelang/article/details/49000203)
[怎样用 Android Annotations 写出高性能代码](http://blog.csdn.net/feelang/article/details/49095235)
[安卓App热补丁动态修复技术介绍](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400118620&idx=1&sn=b4fdd5055731290eef12ad0d17f39d4a&scene=0&uin=MTYzMjY2MTE1&key=04dce534b3b035ef49d8b47c3f8dc1399d737e94c7a40b1a38561c6fcf48d000a1f40ec4bf530d2534dd865875c0c8c7&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&lang=en&pass_ticket=1zsiC5hQfwATA4R3ndq32UtcvN%2B5kATcavEv4xN2HMY%3D)

[Android中如何提取和生成mp4文件](http://ticktick.blog.51cto.com/823160/1710743)
[ Android 热补丁动态修复框架小结](http://blog.csdn.net/lmj623565791/article/details/49883661)
[Android App 线上热修复方案](http://mp.weixin.qq.com/s?__biz=MzA3Mjk1MjA4Nw==&mid=400390453&idx=1&sn=ad5e93193f46ba1bdccafda26508d702#rd)

# Android studio教程 #
[配置出“NB”的Android Studio](http://blog.csdn.net/yy1300326388/article/details/46374229) 

# RxJava 教程 #
[给 Android 开发者的 RxJava 详解](http://gank.io/post/560e15be2dca930e00da1083#toc_1) 
[RxJava学习资源](https://github.com/lzyzsd/Awesome-RxJava)
[用 RxJava 实现 EventBus ](https://github.com/mcxiaoke/xBus)
[用 RxJava 实现 BroadcastReceiver](https://github.com/f2prateek/rx-receivers)
[Rxlifecycle使用详解，解决RxJava内存泄露问题](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1122/3711.html)
[Getting Started With ReactiveX on Android](http://code.tutsplus.com/tutorials/getting-started-with-reactivex-on-android--cms-24387)

# Handler #
[Android Handler消息机制的理解](http://anany.me/2015/04/12/handler/)


# Adapter #
[Adapter优化方案的探索](https://github.com/tianzhijiexian/Android-Best-Practices/blob/master/2015.10/adapter/adapter.md)

# 开源项目 #
[开源选型之 Android 三大图片缓存原理、特性对比](http://mp.weixin.qq.com/s?__biz=MzAxNjI3MDkzOQ==&mid=400055274&idx=1&sn=89005ccb6b4317675c54ccf61cdb89b5#rd)
[Glide 一个专注于平滑滚动的图片加载和缓存库](http://www.jianshu.com/p/4a3177b57949)
[Android实战之你应该使用哪个网络库？](http://segmentfault.com/a/1190000003965158)
[okHttp，GreenDao，EventBus简单封装使用](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1111/3678.html)
[Retrofit 入门教程](https://futurestud.io/blog/retrofit-getting-started-and-android-client/)
[好用的网络请求库Retrofit2（入门及讲解）](http://blog.csdn.net/biezhihua/article/details/49232289)

# 设计师 #
[APP界面切图命名和文件整理规范](http://www.shejipai.cn/map-file-naming-and-specification.html)
[双管齐下：同时设计 iOS 和 Android](http://www.shejipai.cn/ios-android-compare-ui.html)


# 书 #
[程序员的自我修养](https://www.gitbook.com/book/leohxj/a-programmer-prepares/details?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# 原理 #
[公共技术点之 View 绘制流程](http://www.codekk.com/blogs/detail/54cfab086c4761e5001b253f)
[Android热更新实现原理](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1115/3684.html)

# 优化 #
[给 App 提速：Android 性能优化总结](http://android.jobbole.com/81944/)
[Android打包的那些事](http://www.jayfeng.com/2015/11/07/Android%E6%89%93%E5%8C%85%E7%9A%84%E9%82%A3%E4%BA%9B%E4%BA%8B/)
[加速你的Android应用](http://www.devtf.cn/?p=1097)
[内存泄露从入门到精通三部曲之基础知识篇](http://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&mid=400674207&idx=1&sn=a9580ca0dffc62a6d7dbb8fd3d7a2ef1&scene=0&key=b410d3164f5f798e3f4b6de393face7f291ae1d5d6ce312646e1e72ba2b6849e52d3ef5d2d0e4e8579cc7841aac8b439&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&pass_ticket=hgYTL4MW7%2FI9mnat%2BT9S2RRS0IkFfm6yOLSy%2F4bguL4%3D)
[关于Android Log的一些思考](http://droidyue.com/blog/2015/11/01/thinking-about-android-log/)
[Android项目重构之路:架构篇](http://keeganlee.me/post/android/20150605)
[内存泄露从入门到精通三部曲之排查方法篇](http://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&mid=400891536&idx=1&sn=0b6c629b0abe4a359d6552cd244c0c0c&scene=0&key=d4b25ade3662d6432f4d008c35c73be9edb35e268795decfd642e018f5b9b57ccf844430313ae8cae1936ae1af28f657&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&pass_ticket=DhP26XYXJwz4Wb0cgRmjgcxeGfVbtRncCyGulGN45GY%3D)
[内存泄露从入门到精通三部曲之常见原因与用户实践](http://bugly.qq.com/blog/?p=884)
[10 条提升 Android 性能的建议](https://realm.io/cn/news/droidcon-farber-improving-android-app-performance/)
[Android应用启动优化:一种DelayLoad的实现和原理](http://androidperformance.com/2015/11/18/Android-app-lunch-optimize-delay-load.html)
[Android性能调优利器StrictMode](http://www.kuqin.com/shuoit/20150928/348295.html)

# 提高 #
[深入理解Android之AOP](http://blog.csdn.net/innost/article/details/49387395)
[移动端图片格式调研](http://blog.ibireme.com/2015/11/02/mobile_image_benchmark/)

# 新特性 #
[Android M新特性Doze and App Standby模式详解](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400185947&idx=1&sn=a591b76d2c9a085791fd4f12a5b31738&scene=2&srcid=11067beUUcVUcBRI1ajZZ2p7&from=timeline&isappinstalled=0&key=b410d3164f5f798e6f3fbdb81070f8443873c0d4632acc14a6513981556fa35169ba650e853f94945b244528cbd58799&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&pass_ticket=hgYTL4MW7%2FI9mnat%2BT9S2RRS0IkFfm6yOLSy%2F4bguL4%3D)


# 架构 #
[微信为啥这么省流量（技术宅入）](http://mp.weixin.qq.com/s?__biz=MjM5ODYxMDA5OQ==&mid=400163013&idx=1&sn=911cf71925e2ba50d47955a713134acb&scene=2&srcid=1024VUjDjr5hy3hpqvaZ72D3&from=timeline&isappinstalled=0#rd)
[Android 项目重构之路：界面篇](http://android.jobbole.com/82080/)
[各大热补丁方案分析和比较](http://blog.zhaiyifan.cn/2015/11/20/HotPatchCompare/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)


# 适配 #
[安卓分辨率的相关知识](http://leoray.leanote.com/post/android-resolution)
[安卓资源及适配的一些问题](http://leoray.leanote.com/post/android-resource)
[AndroidAutoLayout：Android 屏幕适配方案](https://github.com/hongyangAndroid/AndroidAutoLayout?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# 博客 #
[leanote](http://leoray.leanote.com/)

# 官方学习网站/Wiki #
[Android Developer](http://developer.android.com/)
[Android Developer(无需梯子)](http://androiddoc.qiniudn.com/index.html)
[Android Training 中文版](http://hukai.me/android-training-course-in-chinese/index.html)
[Material Design 中文版](http://wiki.jikexueyuan.com/project/material-design/)
[值得阅读的android技术文章 ](https://github.com/bboyfeiyu/Worth-Reading-the-Android-technical-articles)
[整理一些比较好的Android开发教程 ](http://bxbxbai.github.io/2014/10/07/android-develop-resource/)
[2015年最新Android基础入门教程目录(完结版)](http://blog.csdn.net/coder_pig/article/details/50000773#t8)

# 面试题 #
[很详细的Android工程师面试题大全](http://blog.csdn.net/mc_hust/article/details/49517915)
[Android 面试常见问题](https://github.com/leerduo/InterviewQuestion)

