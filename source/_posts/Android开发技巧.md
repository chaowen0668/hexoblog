title: android开发技巧
date: 2015-09-08 13:06:26
tags:
categories: android


---
# UI技巧 #
[Android键盘面板冲突 布局闪动处理方案](https://github.com/Jacksgong/JKeyboardPanelSwitch)
[ Android 透明状态栏实现方案](http://email.mail.gank.io/c/eJwNjjsOwyAQRE9jSrSLlzUUFG5yjQjwD8XGsU2R42elkeZN9WYKlHPfsyrBADIQOCD0aLVBGpz23hFrO4IZrR07giOWXa-xfnQ51RYg4wATcbSIC2MagAy7NDhgRvRJHQGlyTi1h621b9ePnXlJ0n6uOj9T1XVuspdYf6W-vRGOdyt5n4WmuYnwEbIIjpFI3UFcTPKO5M916XwefyyRNf8)
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
[Android布局优化之ViewStub、include、merge使用与源码分析](http://blog.csdn.net/bboyfeiyu/article/details/45869393#0-tsina-1-42567-397232819ff9a47a7b7e80a40613cfe1)
[腾讯Bugly干货分享：Android机型适配之痛](http://www.csdn.net/article/2015-09-08/2825645/1)
[如何更新及替换ViewPager中的Fragment](https://segmentfault.com/a/1190000003742057)
[Android中WebView页面交互](http://segmentfault.com/a/1190000004150350)
[Android 软键盘和emoji表情切换方案，和微信几乎一样的体验](Android 软键盘和emoji表情切换方案，和微信几乎一样的体验)
[Android -- 固定在ScrollView顶部的View，类似于新浪微博的评论列表的顶部](http://my.oschina.net/Hideeee/blog/500933?fromerr=YG7GdWlK)
[自定义组件最详细实例讲解（7步实现自定义ViewGroup）](http://leoray.leanote.com/post/viewgroup-custom)
[在滚动列表中实现视频的播放(ListView & RecyclerView)](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0130/3927.html)
[Android开发中一些被冷落但却很有用的类和方法](http://t.cn/RbsSFw0)
[Android夜间模式最佳实践]()
[Android开发：最详细的 Toolbar 开发实践总结](http://www.jianshu.com/p/79604c3ddcae)
[这可能是目前最鲁棒的Android声音录制和播放封装库了](http://blog.piasy.com/Robust-Android-Audio-encapsulation/)
[Android NavigationDrawer 开发实践总结](http://www.jianshu.com/p/c8cbeb7ea43a)
[Android 界面性能调优资料](https://testerhome.com/topics/4304?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Android APP 快速 Pad 化实现](https://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&mid=404548816&idx=1&sn=f042037982ed2e74210c57edf864e31a&scene=0&key=710a5d99946419d952212e00d975092230dca20db96a430d17bf4528f8b81e3323355b8ec4c4336a06461c81e5d2c9c2&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.3+build(15D21)&version=11020201&pass_ticket=mkxSG9yBAX1Owyn8FYzTXI641ZdTMCjVwh5JSkA24pE%3D)
[夜晚的故事(android夜间模式实现)](http://www.jianshu.com/p/60608820bb71)

## 关于RadioButton setCheck方法的问题 ##
在做项目过程中，使用radioButton来做菜单切换导航，发现在RadioButton在与其他按钮来回切换会背景不生效,可以使用以下代码
```
rg.clearCheck();//清除选中状态的 
```

[参考来源](http://stackoverflow.com/questions/4035465/android-radiobutton-not-able-to-unset-using-setcheckedfalse-method)


# 代码优化 #
[Android Bitmap面面观](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0329/4101.html)
[ 利用 Android Annotations 来玩玩契约编程](http://blog.csdn.net/feelang/article/details/49000203)
[怎样用 Android Annotations 写出高性能代码](http://blog.csdn.net/feelang/article/details/49095235)
[安卓App热补丁动态修复技术介绍](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400118620&idx=1&sn=b4fdd5055731290eef12ad0d17f39d4a&scene=0&uin=MTYzMjY2MTE1&key=04dce534b3b035ef49d8b47c3f8dc1399d737e94c7a40b1a38561c6fcf48d000a1f40ec4bf530d2534dd865875c0c8c7&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&lang=en&pass_ticket=1zsiC5hQfwATA4R3ndq32UtcvN%2B5kATcavEv4xN2HMY%3D)

[Android中如何提取和生成mp4文件](http://ticktick.blog.51cto.com/823160/1710743)
[ Android 热补丁动态修复框架小结](http://blog.csdn.net/lmj623565791/article/details/49883661)
[Android App 线上热修复方案](http://mp.weixin.qq.com/s?__biz=MzA3Mjk1MjA4Nw==&mid=400390453&idx=1&sn=ad5e93193f46ba1bdccafda26508d702#rd)
[解决 singleTask onActivityResult() 无效的问题](http://mthli.github.io/singleTask-onActivityResult/)
[判断指定App是否位于前台的方法](https://github.com/wenmingvs/AndroidProcess)
[Android开发的那些坑和小技巧](http://www.cnblogs.com/lao-liang/p/4941653.html?f=tt&hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[你应该知道的那些Android小经验](https://mp.weixin.qq.com/s?__biz=MzA4MjU5NTY0NA==&mid=404388098&idx=1&sn=8bbbba7692dca68cdda2212dec4d86c0&scene=1&srcid=0320gXPloap70ixGeYnNUaAW&key=710a5d99946419d972fe638b34e38edcf7064c302f8526f10b927c7e27886585b83b5b60bc342db482d2a7846e24c284&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.3+build(15D21)&version=11020201&pass_ticket=pvdhfR4lRer%2FtYDsP5cnFux5OK0GM%2FUQMgt5TOvHlpQ%3D)
[android:process 的坑，你懂吗？](http://sendcloud_track.batch.manong.io/track/click/eyJ1c2VyX2lkIjogMTg3LCAidGFza19pZCI6ICIiLCAiZW1haWxfaWQiOiAiMTQ1ODY1OTkwNjU3MF8xODdfODk3M18yMjM2LnNjLTEwXzEwXzI0XzE1Ni1pbmJvdW5kMCQ1MTE2NDQ3ODRAcXEuY29tIiwgInNpZ24iOiAiMTE1MzMzNTU4ODg0OTViY2FkZGRiMGRmZmFjODAyNWIiLCAidXNlcl9oZWFkZXJzIjoge30sICJsYWJlbCI6ICIxNjgzMyIsICJsaW5rIjogImh0dHAlM0EvL3dlZWtseS5tYW5vbmcuaW8vYm91bmNlJTNGdXJsJTNEaHR0cCUyNTNBJTI1MkYlMjUyRnd3dy5yb2dlcmJsb2cuY24lMjUyRjIwMTYlMjUyRjAzJTI1MkYxNyUyNTJGYW5kcm9pZC1wcm9lc3MlMjUyRiUyNmFpZCUzRDU1NzElMjZuaWQlM0QxMTAiLCAiY2F0ZWdvcnlfaWQiOiA2MDU4OX0=.html)
[关于Android开发的40条优化建议](http://t.cn/RqPvBEl)
[APK瘦身记，如何实现高达53%的压缩效果](https://mp.weixin.qq.com/s?__biz=MzIwMTI4Nzk5Ng==&mid=402517579&idx=1&sn=2951ec2b3aef4ce6f6a5c06ad4c49d73&scene=1&srcid=03306GCdiG6G4yhZIaDsHVL9&key=710a5d99946419d9193b805ec5a41fb34a812c3dc4608557894831240095cf354407df239d9d78b9f6ab8b7a69a918be&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.4+build(15E65)&version=11020201&pass_ticket=AOchp9l%2F7Ug8gVFlX0%2BK1tAyLOPwStguLTy4jV5RBLc%3D)
[Android MultiDex实践：如何绕过那些坑？](https://mp.weixin.qq.com/s?__biz=MzA4MjU5NTY0NA==&mid=405574783&idx=1&sn=6ff49fda8a7229bf6b2692fddcf23e04&scene=1&srcid=0406rIx0Y8UeeSwlQkcWZO3D&key=710a5d99946419d9c98f609fa48d8a98a8b1b1337c7c4ffffdd190537eabc103ed788c6434410e1129cd0428da695802&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.4+build(15E65)&version=11020201&pass_ticket=%2FiqZ3iooRz56i55SDTJXia%2F538BgsKzUx5BjjlLzrNU%3D)

# Android studio教程 #
[配置出“NB”的Android Studio](http://blog.csdn.net/yy1300326388/article/details/46374229) 

# RxJava 教程 #
[给 Android 开发者的 RxJava 详解](http://gank.io/post/560e15be2dca930e00da1083#toc_1) 
[RxJava学习资源](https://github.com/lzyzsd/Awesome-RxJava)
[用 RxJava 实现 EventBus ](https://github.com/mcxiaoke/xBus)
[用 RxJava 实现 BroadcastReceiver](https://github.com/f2prateek/rx-receivers)
[Rxlifecycle使用详解，解决RxJava内存泄露问题](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1122/3711.html)
[Getting Started With ReactiveX on Android](http://code.tutsplus.com/tutorials/getting-started-with-reactivex-on-android--cms-24387)
[ 可能是东半球最全的RxJava使用场景小结](http://blog.csdn.net/theone10211024/article/details/50435325)
[RxJava Essentials 一书的中文翻译版](https://www.gitbook.com/book/yuxingxin/rxjava-essentials-cn/details?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Awesome-RxJava](https://github.com/lzyzsd/Awesome-RxJava)
[使用RxJava 提升用户体验](http://www.jianshu.com/p/33c548bce571)
[我们为什么要在Android中使用RxJava](http://blog.csdn.net/jijiaxin1989/article/details/50517068#0-tsina-1-18574-397232819ff9a47a7b7e80a40613cfe1)
[RxJava 与 Retrofit 结合的最佳实践](http://gank.io/post/56e80c2c677659311bed9841)
[一个用于学习RxJava操作符的APP](https://github.com/jiang111/RxJavaApp)
[从案例学习RxAndroid](http://androidweekly.us9.list-manage.com/track/click?u=3f24a71686f577759d1824501&id=f45c87bab2&e=c10fafc873)
[RxJava常见的使用场景总结](http://www.jianshu.com/p/6917510b0e4c)
[我们的安卓客户端是如何使用 RxJava 的](https://realm.io/cn/news/kau-felipe-lima-adopting-rxjava-airbnb-android/)
[RxJava中的错误处理](http://www.jianshu.com/p/916b72778145)

# Handler #
[Android Handler消息机制的理解](http://anany.me/2015/04/12/handler/)
[Android Handler消息机制的理解](http://blog.csdn.net/jianhua0902/article/details/49508945)
[Android消息循环机制源码分析](http://mouxuejie.com/blog/2016-03-31/message-looper-mechanism/)


# Adapter #
[Adapter优化方案的探索](https://github.com/tianzhijiexian/Android-Best-Practices/blob/master/2015.10/adapter/adapter.md)

# 开源项目 #
[开源选型之 Android 三大图片缓存原理、特性对比](http://mp.weixin.qq.com/s?__biz=MzAxNjI3MDkzOQ==&mid=400055274&idx=1&sn=89005ccb6b4317675c54ccf61cdb89b5#rd)
[Glide 一个专注于平滑滚动的图片加载和缓存库](http://www.jianshu.com/p/4a3177b57949)
[Android实战之你应该使用哪个网络库？](http://segmentfault.com/a/1190000003965158)
[okHttp，GreenDao，EventBus简单封装使用](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1111/3678.html)
[Retrofit 入门教程](https://futurestud.io/blog/retrofit-getting-started-and-android-client/)
[好用的网络请求库Retrofit2（入门及讲解）](http://blog.csdn.net/biezhihua/article/details/49232289)
[安卓下拉刷新开源库对比](https://github.com/desmond1121/Android-Ptr-Comparison/blob/master/README.md)
[Volley+OkHttp3+Gson（Jackson）开源库的封装过程](http://allenlin.leanote.com/post/volleyokhttpgson)
[如何更高效地使用 OkHttp](http://brucezz.github.io/articles/2016/02/21/effective-okhttp/)
[Glide 深入研究 ](http://email.mail.gank.io/c/eJwVjksOgzAMBU9DlpEdOx8WWbRS4QA9AAqQ0qgECkrv3yD5-Y28Gc-ep4nIiOQVoAGGK04biWSIpMaKYB4Ou7trGHJIq1zC9pFpF2-PVrfBtIgGSY0WYOTZOXY6ArU0RZE9IrasnFj9u5RvQ7dGdXXy-frJHCtd3lqgLrZ19Wua49DHUtK2DM8SzhLnehen19XEbB3XV45DTnv-A44rM2k)
[Glide 系列使用教程](https://mail.qq.com/cgi-bin/frame_html?sid=jv49Mye5pdrXChRD&r=814efd55a7c3af31c3e5490bfc25de07)

# 设计师 #
[APP界面切图命名和文件整理规范](http://www.shejipai.cn/map-file-naming-and-specification.html)
[双管齐下：同时设计 iOS 和 Android](http://www.shejipai.cn/ios-android-compare-ui.html)


# 书 #
[程序员的自我修养](https://www.gitbook.com/book/leohxj/a-programmer-prepares/details?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# 原理 #
[公共技术点之 View 绘制流程](http://www.codekk.com/blogs/detail/54cfab086c4761e5001b253f)
[Android热更新实现原理](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/1115/3684.html)
[Android源码分析-全面理解Context](http://www.cnblogs.com/android100/p/Android-Context.html)
[Android杂谈--Activity、Window、View的关系](http://www.cnblogs.com/loulijun/archive/2012/02/09/2344681.html)
[Android应用开发Scroller详解及源码浅析](http://blog.csdn.net/yanbober/article/details/49904715)
[ Android应用开发之自定义View触摸相关工具类全解](http://blog.csdn.net/yanbober/article/details/50411919)
[理解Android安全机制](http://android.jobbole.com/82409/)
[Android Scroller完全解析，关于Scroller你所需知道的一切](http://blog.csdn.net/guolin_blog/article/details/48719871)
[阅读Android源码的一些姿势](http://zhuanlan.zhihu.com/kaede/20564614?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[深入理解LayoutInflater.inflate()](http://blog.chengdazhi.com/index.php/110?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[关于获取当前Activity的一些思考](http://droidyue.com/blog/2016/02/21/thinking-of-getting-the-current-activity-in-android/)
[ViewAnimator源码分析](http://t.cn/RqhoVje)
[AsyncTask源码剖析](http://email.mail.gank.io/c/eJw1j02KwzAMhU8TL40k26q98CIDLcxuFr2A6oQ2pEl_0ln09pVgBuyn76EnGQ81thYCu6kSIEOgpDcm8mTsOWPmLsIi09WfZZ39dHOXCokzMMkQsxQgKSOPNJIA44DtBG6piFgiZXetl9fr3oW-o4Oe7S7P-f0rq19GtfaoFgjGJv32XttRtrmjtNdW-tLBVMDsTqU3ymg2GRXr8n-47P_Cuf_5ViSwpZo5uGdNiBzjLkf9z-Ph2235AEOPPvw)

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
[Android性能优化之被忽视的优化点](http://android.jobbole.com/82182/)
[Android性能优化之如何避免Overdraw](http://www.jianshu.com/p/145fc61011cd)
[Android 中 SQLite 性能优化](http://droidyue.com/blog/2015/12/13/android-sqlite-tuning/)
[手机淘宝性能优化](http://yq.aliyun.com/articles/53?&utm_campaign=sys&utm_medium=market&utm_source=edm_email&msctype=email&mscmsgid=108015121700582161&)
[手淘双十一系列（一） | 521 性能优化项目揭秘](http://yq.aliyun.com/articles/1477?spm=5176.100238.yqhn2.41.TapcjW)
[Android退出应用最优雅的方式](http://android.jobbole.com/82316/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Android 开发绕不过的坑：你的 Bitmap 究竟占多大内存？](http://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&mid=403263974&idx=1&sn=b0315addbc47f3c38e65d9c633a12cd6)
[BlockCanary — 轻松找出Android App界面卡顿元凶](http://blog.zhaiyifan.cn/2016/01/16/BlockCanaryTransparentPerformanceMonitor/)
[使用pngquant来缩小你的APK](http://www.jianshu.com/p/a721fbaa62ab)
[Android性能优化典范](http://hukai.me/android-performance-patterns-season-4/)
[Android UI性能优化详解](http://music4kid.github.io//android/2016/01/11/android-performance-ui/)
[[个人总结]APK瘦身实践](http://www.jayfeng.com/2015/12/29/APK%E7%98%A6%E8%BA%AB%E5%AE%9E%E8%B7%B5/)
[Android中导致内存泄漏的竟然是它----Dialog](https://mp.weixin.qq.com/s?__biz=MzA3NTYzODYzMg==&mid=403426100&idx=1&sn=aceffb315d63fa0139b0e1c2b0edce64&scene=0&key=710a5d99946419d909c81f932a79710be0582b714c090ef6ac916b002ebd168fd146b8132d3282cc861544ba194025e0&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.2+build(15C50)&version=11020201&pass_ticket=3czwvrJ0y4smIOu90jD4B8NFtnWfzwg%2FT2S2qlILyyY%3D)
[优化 Android 线程和后台任务开发](https://realm.io/cn/news/android-threading-background-tasks/)
[Android 内存泄漏总结](https://yq.aliyun.com/articles/3009?spm=5176.100238.yqhn2.14.yN83zE&comefrom=http://blogread.cn/news/)
[Android APK终极瘦身21招](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=402380504&idx=1&sn=7013f0842867a21555adcf445c7c03ee#rd)
[Android 内存泄漏案例和解析](https://drakeet.me/android-leaks)
[Android开发——避免内存泄露](http://www.cnblogs.com/JohnTsai/p/5256295.html)

# 提高 #
[深入理解Android之AOP](http://blog.csdn.net/innost/article/details/49387395)
[移动端图片格式调研](http://blog.ibireme.com/2015/11/02/mobile_image_benchmark/)
[如何选择 compileSdkVersion, minSdkVersion 和 targetSdkVersion](http://chinagdg.org/2016/01/picking-your-compilesdkversion-minsdkversion-targetsdkversion/)
[Android平台的崩溃捕获机制及实现](http://mp.weixin.qq.com/s?__biz=MzA4MzEwOTkyMQ==&mid=416184980&idx=1&sn=193b2a8aa3ac91fe54f647068c659633)
[携程Android App插件化和动态加载实践](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=401890966&idx=1&sn=b8d888acb7d4ace5d4e579a5588bf90b&scene=1&srcid=0219aSN6dGolDZQV0GnyqDPP&from=groupmessage&isappinstalled=0#wechat_redirect)
[Binder学习指南](http://weishu.me/2016/01/12/binder-index-for-newer/)
[Android使用FFMpeg实现推送视频直播流到服务器](http://sixwolf.net/blog/2016/01/30/Android%E4%BD%BF%E7%94%A8FFMpeg%E5%AE%9E%E7%8E%B0%E6%8E%A8%E9%80%81%E8%A7%86%E9%A2%91%E7%9B%B4%E6%92%AD%E6%B5%81%E5%88%B0%E6%9C%8D%E5%8A%A1%E5%99%A8/)
[这里收集了大家常用的一些Android的模板代码](https://github.com/jiang111/awesome-android-tips)
[Android实现多次闪退清除数据](http://email.mail.gank.io/c/eJw9kEluwzAMRU9jLwVSoqaFFkrq3MNTEqO21aQGmuOHDGoDwiMfPjVAQ6K-N8bVU9KADow2QAQQFAISl2jAgzKogbw_VwRLO83q1q7fair1PcXOO-NdjP0YRnDYeeN4FnSwbX-1Q70kRIykQz2n-7b9VCZX-sLrd3r9lfmq1nFj6-Zy4yKP4AJGes3I6_As01Bp21hGbhhR0HhGkO4ER0qSZlEnehagaJRAduS8a4Adn-FTELXHcNzP-6TRHheJhq__t1zqZ7KIjsgH4t95PFRfljdBj1EE)
[Android路由框架设计与实现](http://email.mail.gank.io/c/eJxVj90OwiAMhZ9mXBJaoIMLLmayvcf-VOI2nC7Rx7c18cKkPT0fbdMwJTeO1pLKCQ2Qseg5nUeN4jUFCFQ5s_Z50Zd-u-lc1DXBRN6EuY449J6nI0KcZxwGRO851JoAIDoMaknX47hXtqmw43jm96ssZ73NB9OwlAsXOc3FWPEizTY9Sp4q9G1gOdUsTScoLjp5A0GShrhAP4ytdOm323yx_UPZ6NQjeQByrg6Of7jveizrB5zhQrs)
[Android 插件化原理解析——插件加载机制](http://weishu.me/2016/04/05/understand-plugin-framework-classloader/)

# 新特性 #
[Android M新特性Doze and App Standby模式详解](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400185947&idx=1&sn=a591b76d2c9a085791fd4f12a5b31738&scene=2&srcid=11067beUUcVUcBRI1ajZZ2p7&from=timeline&isappinstalled=0&key=b410d3164f5f798e6f3fbdb81070f8443873c0d4632acc14a6513981556fa35169ba650e853f94945b244528cbd58799&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&pass_ticket=hgYTL4MW7%2FI9mnat%2BT9S2RRS0IkFfm6yOLSy%2F4bguL4%3D)
[聊一聊Android 6.0的运行时权限](http://droidyue.com/blog/2016/01/17/understanding-marshmallow-runtime-permission/)
[AppBar简述](http://www.jianshu.com/p/4ce0f3419ca8)
[AppBar的详解](https://github.com/SpikeKing/TestAppBar)
[Android 6.0: 动态权限管理的解决方案](http://www.jianshu.com/p/dbe4d37731e6)
[Android 6.0 运行时权限处理完全解析](http://blog.csdn.net/lmj623565791/article/details/50709663)
[Android Support Library 23.2有哪些新东西](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0226/3996.html)
[AndroidStudyDemo之Android4.x介绍](http://email.mail.gank.io/c/eJwVjjsOwyAQRE9jSsTCLp-Cgib3wEuISfxNHPn6IdJM8zTSmxKR2RgrWtQKrELlFUIAkhrQeRmCRyspKZ2I0oBqyW2Wj7y-ZNvEFB0b9g5xJOMz6Orp7kxFtrVQcbqIJQJAQO3FHKfz3AeTBn3rua5LPlteP9NX8rZ0svc6zpY01VJ4FO9IABb7D-zm4_jvfgyMMFA)
[MVVM-DBinding](https://github.com/tianzhijiexian/DBinding)
[HotFix的抉择](http://mp.weixin.qq.com/s?__biz=MzIxNDE1NjQ2Mw==&mid=2649872243&idx=1&sn=e4998ed201087249de74731beb9ea423#rd)

# 架构 #
[微信为啥这么省流量（技术宅入）](http://mp.weixin.qq.com/s?__biz=MjM5ODYxMDA5OQ==&mid=400163013&idx=1&sn=911cf71925e2ba50d47955a713134acb&scene=2&srcid=1024VUjDjr5hy3hpqvaZ72D3&from=timeline&isappinstalled=0#rd)
[Android 项目重构之路：界面篇](http://android.jobbole.com/82080/)
[各大热补丁方案分析和比较](http://blog.zhaiyifan.cn/2015/11/20/HotPatchCompare/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[用MVP架构开发Android应用](http://kymjs.com/code/2015/11/09/01/)
[Android应用架构](http://www.jianshu.com/p/8ca27934c6e6)
[说说Android的MVP模式](http://toughcoder.net/blog/2015/11/29/understanding-android-mvp-pattern/)
[说说Android的MVP模式](http://toughcoder.net/blog/2015/11/29/understanding-android-mvp-pattern/)
[几幅图MVC，MVP 和 MVVM框架一下子全明白了！](http://www.ruanyifeng.com/blog/2015/02/mvcmvp_mvvm.html)
[饿了么移动APP的架构演进](https://mp.weixin.qq.com/s?__biz=MzAxNDUwMzU3Mw==&mid=401044540&idx=1&sn=24b7d8fb655ae6dd5d989d0cb3c08e90)
[Android架构合集](https://github.com/Juude/Awesome-Android-Architecture)
[Android应用架构](http://blog.zhaiyifan.cn/2016/01/29/android-app-architecture-2015/?from=groupmessage&isappinstalled=0)
[Android干净架构详解：为你的应用打造一个清爽的架构！](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=402486518&idx=1&sn=e466c3cfcbe02126d92f81cfc347fba4#rd)
[不要写死！天猫App的动态化配置中心实践](https://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=402842876&idx=1&sn=e15d596c95bf7d1ed579cfd7e410696a&scene=1&srcid=0315cLs789Ej7XkMleLpkxHE&key=710a5d99946419d97e9c08070121534434102c68991612315319a18a6a15d57b74a1908cf0323fb6069efa758e34889c&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.3+build(15D21)&version=11020201&pass_ticket=k0qKNM4TZo426DYTd0YLgC8zV3UKUywv%2Fk7W7VEvbY8%3D)
[Android App的设计架构：MVC,MVP,MVVM与架构经验谈](http://sendcloud_track.batch.manong.io/track/click/eyJ1c2VyX2lkIjogMTg3LCAidGFza19pZCI6ICIiLCAiZW1haWxfaWQiOiAiMTQ1ODY1OTkwNjU3MF8xODdfODk3M18yMjM2LnNjLTEwXzEwXzI0XzE1Ni1pbmJvdW5kMCQ1MTE2NDQ3ODRAcXEuY29tIiwgInNpZ24iOiAiMjZkN2EzMWViNWQxY2YxMGQ0NDdhMGRhMGIyMzY1NzQiLCAidXNlcl9oZWFkZXJzIjoge30sICJsYWJlbCI6ICIxNjgzMyIsICJsaW5rIjogImh0dHAlM0EvL3dlZWtseS5tYW5vbmcuaW8vYm91bmNlJTNGdXJsJTNEaHR0cCUyNTNBJTI1MkYlMjUyRnd3dy50aWFubWF5aW5nLmNvbSUyNTJGdHV0b3JpYWwlMjUyRkFuZHJvaWRNVkMlMjZhaWQlM0Q1NTY5JTI2bmlkJTNEMTEwIiwgImNhdGVnb3J5X2lkIjogNjA1ODl9.html)
[App架构经验总结](http://toutiao.io/r/cwmt3k)
[Android MVP架构中的Presentation层应该怎么设计](https://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=402868193&idx=1&sn=790e12f84dfcea171528e6d3789c69ed&scene=1&srcid=0318edkkVeWbjOhcNH6WDTZQ&key=710a5d99946419d971dd3aa71f3cb0b2e509051adcdbc9164c1787ffeeaf37389747b35a2c1c899c3ec825d8bc190ec1&ascene=0&uin=Mjc3OTU3Nzk1&devicetype=iMac+MacBookPro9%2C2+OSX+OSX+10.10.3+build%2814D136%29&version=11020201&pass_ticket=e3qL7YcbmknxduKwWiyzQxJoeiIW7hRFdqBaO206p868fDQqQ7UIiIsPe%2FiSY23E)
[我的 Android 开发实战经验总结](http://email.mail.gank.io/c/eJwVjUsOwyAMBU8TlsjGBpwFi6hS7xFANLT5tqly_VLpzWY00suBUyJyqgYD6ICMALEH0AjIzmqx1lvNg5Hhxr5jWMY668e4vnTd1BQguwSOwIONKZLLMRmxvfReCHJxagmI2LMRNYfpPPeOhs7c267r0s86rp_pq9O2NLM3uKA1MUnhQp0h9Q4W0TF74XZ-HP_0B4hZMDo)
[微信Android客户端后台保活经验分享](https://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=403254393&idx=1&sn=8dc0e3a03031177777b5a5876cb210cc&scene=1&srcid=0402uDoqRaKQffY51mJ0N8G6&key=710a5d99946419d98b567bf76a8e4f11bb50879bb6d2238881b4ab84e10cc0840e943ea3003a0106d73399e336311cec&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.4+build(15E65)&version=11020201&pass_ticket=gGDjhIlTQ7vPThoj%2FZ5xrdCNNXWwfjAXhqZnbyhnJmQ%3D)
[Android MVP 详解（上）](http://androidweekly.us9.list-manage.com/track/click?u=3f24a71686f577759d1824501&id=5a7252222e&e=c10fafc873)
[Android MVP 详解（下）](http://androidweekly.us9.list-manage.com/track/click?u=3f24a71686f577759d1824501&id=587e2b135a&e=c10fafc873)
[我眼中的Android架构](http://blog.chengdazhi.com/index.php/150)
[Android官方MVP架构示例项目解析](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=403539764&idx=1&sn=d30d89e6848a8e13d4da0f5639100e5f&scene=0#wechat_redirect)
[Android官方MVP架构示例项目解析](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=403539764&idx=1&sn=d30d89e6848a8e13d4da0f5639100e5f#rd)
[选择恐惧症的福音！教你认清MVC，MVP和MVVM](http://zjutkz.net/2016/04/13/%E9%80%89%E6%8B%A9%E6%81%90%E6%83%A7%E7%97%87%E7%9A%84%E7%A6%8F%E9%9F%B3%EF%BC%81%E6%95%99%E4%BD%A0%E8%AE%A4%E6%B8%85MVC%EF%BC%8CMVP%E5%92%8CMVVM/#more)
[Android App的设计架构：MVC,MVP,MVVM与架构经验谈](https://www.sdk.cn/news/2501)

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
[衡量android开发者水平的面试问题](http://blog.csdn.net/lpjishu/article/details/50316919)
[Activity LaunchMode 应用场景](http://xiazdong.me/2015/03/08/android-launchmode-application/)
[Activity的LaunchMode应用场景思考](http://blog.csdn.net/xiaodongrush/article/details/28597855)
[Android 编程下 Touch 事件的分发和消费机制](Android 编程下 Touch 事件的分发和消费机制)
[ndroid子线程真的不能更新UI么](http://android.jobbole.com/82431/)
[程序员怎么获得高工资](http://sendcloud_track.batch.manong.io/track/click/eyJ1c2VyX2lkIjogMTg3LCAidGFza19pZCI6ICIiLCAiZW1haWxfaWQiOiAiMTQ1NzQ1MTk2NjA0NF8xODdfMTM3MTBfMjEwMi5zYy0xMF8xMF8yNF8xODQtaW5ib3VuZDAkNTExNjQ0Nzg0QHFxLmNvbSIsICJzaWduIjogIjIzZTQ0ZDhmYTBlOGQ4YTQyODMzYTRhODA4ZmNkMzEyIiwgInVzZXJfaGVhZGVycyI6IHt9LCAibGFiZWwiOiAiMTY4MzMiLCAibGluayI6ICJodHRwJTNBLy93ZWVrbHkubWFub25nLmlvL2JvdW5jZSUzRnVybCUzRGh0dHAlMjUzQSUyNTJGJTI1MkZ3d3cuc3VuaGFvamllLmNvbSUyNTJGMjAxNiUyNTJGMDElMjUyRjA2JTI1MkYlMjUyNUU3JTI1MjVBOCUyNTI1OEIlMjUyNUU1JTI1MjVCQSUyNTI1OEYlMjUyNUU1JTI1MjU5MSUyNTI1OTglMjUyNUU2JTI1MjU4MCUyNTI1OEUlMjUyNUU0JTI1MjVCOSUyNTI1ODglMjUyNUU4JTI1MjU4RSUyNTI1QjclMjUyNUU1JTI1MjVCRSUyNTI1OTclMjUyNUU5JTI1MjVBQiUyNTI1OTglMjUyNUU1JTI1MjVCNyUyNTI1QTUlMjUyNUU4JTI1MjVCNSUyNTI1ODQlMjUyRiUyNmFpZCUzRDU0NzglMjZuaWQlM0QxMDgiLCAiY2F0ZWdvcnlfaWQiOiA2MDU4OX0=.html)
[ Andorid-15k+的面试题。](http://blog.csdn.net/jdsjlzx/article/details/40738053)
[笔试面试知识整理](http://hit-alibaba.github.io/interview/basic/index.html)
[Android开发知识清单整理](http://t.cn/RqhXz7D)
[2016Android某公司面试题](http://yuweiguocn.github.io/2016/04/13/interview-2016-big-company/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# 开发工具 #
[IntelliJ IDEA 简体中文专题教程](https://github.com/judasn/IntelliJ-IDEA-Tutorial)
[日常使用 Git 的 19 个建议](http://blog.jobbole.com/96088/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Android Studio你不知道的调试技巧](http://tianweishu.com/2015/12/21/android-studio-debug-tips-you-may-not-know/)
[Android单元测试研究与实践](http://tech.meituan.com/Android_unit_test.html?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[闯过这 54 关，点亮你的 Git 技能树](http://www.codingstyle.cn/topics/51?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[android studio 64位手机+Fresco引起的在arm64位机器上找不到对应的so库](http://www.cnblogs.com/poe-blog/p/4728970.html)
[Android Studio上打的包在arm64位机器上找不到对应的so库](http://blog.csdn.net/lihuapinghust/article/details/45825063)
[Android中使用Espresso进行UI测试](https://www.aswifter.com/2016/01/03/android-use-Espresso-ui-testing/)
[Git全解析之用起来先](http://wustrive2008.github.io/2016/01/06/%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6/Git%E5%85%A8%E8%A7%A3%E6%9E%90%E4%B9%8B%E5%85%88%E7%94%A8%E8%B5%B7%E6%9D%A5/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Android Studio Gradle实践之多渠道自动化打包+版本号管理](http://unclechen.github.io/2015/10/22/Android%20Studio%20Gradle%E5%AE%9E%E8%B7%B5%E4%B9%8B%E5%A4%9A%E6%B8%A0%E9%81%93%E8%87%AA%E5%8A%A8%E5%8C%96%E6%89%93%E5%8C%85+%E7%89%88%E6%9C%AC%E5%8F%B7%E7%AE%A1%E7%90%86/)
[优雅的Android Studio项目配置--常用库和版本管理](http://www.lcode.org/%E4%BC%98%E9%9B%85%E7%9A%84android-studio%E9%A1%B9%E7%9B%AE%E9%85%8D%E7%BD%AE-%E5%B8%B8%E7%94%A8%E5%BA%93%E5%92%8C%E7%89%88%E6%9C%AC%E7%AE%A1%E7%90%86/)
[使用Android Studio查找文件中含有中文字符串位置](http://waychel.com/shi-yong-android-studiocha-zhao-wen-jian-zhong-han-you-zhong-wen-zi-fu-chuan-wei-zhi/)
[Android studio调试技巧](https://docs.google.com/presentation/d/1Ilb3kBa8C7cArhu7-4TAsA-dDxFkvv9eRL7DC6H56sE/pub?start=false&loop=false&delayms=3000&slide=id.g11baac1e97_0_155)
[更优雅的 Android 发布自动版本号方案](http://www.race604.com/android-auto-version/)
[这些小工具让你的Android开发更高效](http://toutiao.io/r/m5bvmz)
[企业级开发：Gitflow Workflow工作流](http://www.jianshu.com/p/104fa8b15d1e)
[如何在Github打造你的爆款开源项目](https://github.com/gaohailang/blog/issues/9?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[MAT使用入门](http://email.mail.gank.io/c/eJwVjUsOwjAMBU_TLCPbMfkssqAg7uEmgRb6haJenyC92YxGejlySsZYNUQCtMDgwDCj0R4DkTaBvG45XMLVtg3DJMOoHzK_9LCoPhYi521nPLHcMYEHkAy5GCkuixQ1RUQMTF6Nsd_3tTHnhm51x3Ho5yDzp__qtEzVrJXsC7HrsLiO1DueEC2z81yft-3f_QALUjA7)
[Android自动清理无用资源工具](http://email.mail.gank.io/c/eJwVjssOgyAURL9GlgS4Vx4LFrVN_wMvWGkVqvL_KU0mmTOrOdEjEYBm2SshtUBhBCBK4FY6pTg4ZfmE7u4eehpQ7CFv_BXKh-fKVi-AEpFJs4vWkbFkF-NCDGPCJQFGtnsppUNl2ebX1r4D3Ab17Jm3-uJ0xcJLan2vtbxDSZ3C2TJtf4qp9burUxcapbTATt9bIxqL3eY4ONX9B5W4N3U)
[高效Android开发者必须知道的4个工具](http://www.devstore.cn/essay/essayInfo/6102.html)
[Android Studio 配置](http://liukun.engineer/2016/04/10/Android-Studio-advanced-configuration/)
[MAT - Memory Analyzer Tool 使用进阶](http://www.lightskystreet.com/2015/09/01/mat_usage/)

# 学习 #
[Android程序员 如何入门iOS ——故事从这里开始](http://segmentfault.com/a/1190000004268513)
[Android开发技术周报特刊之React Native](http://www.androidweekly.cn/android-dev-special-weekly-react-native/)
[生还是死？Android 进程优先级详解](http://chinagdg.org/2016/01/%E7%94%9F%E8%BF%98%E6%98%AF%E6%AD%BB%EF%BC%9Fandroid-%E8%BF%9B%E7%A8%8B%E4%BC%98%E5%85%88%E7%BA%A7%E8%AF%A6%E8%A7%A3/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Kotlin for android developers》中文版翻译](https://github.com/wangjiegulu/kotlin-for-android-developers-zh)
[定期翻译Android官方博客](https://github.com/smallSohoSolo/android-developer-blog-cn)
[android学习资料](https://github.com/Freelander/Android_Data)
[10个很棒的学习Android 开发的网站](http://mp.weixin.qq.com/s?__biz=MzA4MTg4MjkzMw==&mid=214243534&idx=1&sn=7e8afe532c7809dc1b27456516d42239&scene=4#wechat_redirect)
[Android知识架构](http://lib.csdn.net/base/15/structure)
[开发艺术视频](http://edu.csdn.net/course/detail/1923)

# 数据库 #
[SQLite 大数据量 新增 / 修改 提升效率的办法](http://my.oschina.net/atearsan/blog/187226?fromerr=qCmwUhvO)
[使用replace](http://www.cnblogs.com/liping13599168/archive/2011/05/24/2054908.html)


# 安全 #
[Android应用安全开发之源码安全](http://drops.wooyun.org/mobile/12172)
[Android应用安全开发之防范无意识的数据泄露](http://drops.wooyun.org/mobile/12469)
[Android应用安全开发之浅谈加密算法的坑](https://mp.weixin.qq.com/s?__biz=MzIwMTI4Nzk5Ng==&mid=402506628&idx=1&sn=c5ae6457fa1e112a9b983d46da364125&scene=1&srcid=0329cJms84gOkOWU5y45vSNz&key=710a5d99946419d905ed92f3d6b9c4e2eee8ac517149fdcefd791fbbbb0146dbed8b64ad34aa62bbc9e486eb24c3b03b&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.4+build(15E65)&version=11020201&pass_ticket=AOchp9l%2F7Ug8gVFlX0%2BK1tAyLOPwStguLTy4jV5RBLc%3D)

# 测试 #
[测试技巧 – 你所不知道的测试黑科技](http://blog.chengdazhi.com/index.php/58)
[[团队分享]使用jenkins自动化构建android和ios应用](http://www.jayfeng.com/2015/10/22/%E4%BD%BF%E7%94%A8jenkins%E8%87%AA%E5%8A%A8%E5%8C%96%E6%9E%84%E5%BB%BAandroid%E5%92%8Cios%E5%BA%94%E7%94%A8/)
[世界级的Android测试开发流程（一）](http://blog.zhaiyifan.cn/2016/02/23/world-class-testing-development-pipeline-for-android-part-1/)
[世界级的Android测试开发流程（二）](http://blog.zhaiyifan.cn/2016/02/23/world-class-testing-development-pipeline-for-android-part-2/)
[Roboletric探索之路，从抗拒到依赖](http://iceanson.github.io/Robolectric-%E6%8E%A2%E7%B4%A2%E4%B9%8B%E8%B7%AF)
[Android持续集成以及测试覆盖率可视化](http://sixwolf.net/blog/2016/04/12/Android%E4%BD%BF%E7%94%A8Travis-CI%E6%8C%81%E7%BB%AD%E9%9B%86%E6%88%90%E4%BB%A5%E5%8F%8A%E6%B5%8B%E8%AF%95%E8%A6%86%E7%9B%96%E7%8E%87%E5%8F%AF%E8%A7%86%E5%8C%96/)

# sdk #
[sdk](https://www.sdk.cn/)


# 适配 #
[移动端适配方案(下)](https://github.com/riskers/blog/issues/18)

# 管理 #
[团队分享]如何更好的开发一个Android应用](http://www.jayfeng.com/2016/01/06/%E5%A6%82%E4%BD%95%E6%9B%B4%E5%A5%BD%E7%9A%84%E5%BC%80%E5%8F%91%E4%B8%80%E4%B8%AAAndroid%E5%BA%94%E7%94%A8/#more)
[Android技术积累:开发规范](http://keeganlee.me/post/android/20150709)
[聊聊创业团队的项目管理如何面向开发人员优化](http://toutiao.io/r/15xg4z)
[Android 编码规范](http://email.mail.gank.io/c/eJwVjUkOwjAQBF8TH62Z8Xg7-ICU8A9jO8SQFYLyfRKp61IqqXPglJQyogYCNMCggdgqJZHIsUTFDqTRbdfdWm4YplhH-YzzW9ZFDCGXXAiLsQaKIt8nV2ImbUuybCM-xBQQ0TM5MYZh39dG3Rq6nzuOQ75qnL_DT6ZlOs16AtE77r332pP4BI1omK27nrft6v45YjAN)
[Android技术积累:开发规范](http://t.cn/RqcUJvl)

[客户端API请求规范](http://weekly.manong.io/bounce?url=http%3A%2F%2Fblog.12xiaoshi.com%2F2016%2F03%2F31%2Ftech%2Fapi-constraint_design%2F&aid=5789&nid=112)
[提升代码的可读性系列(一)--基础篇](http://aotu.io/notes/2016/03/31/readable/)

# Reactnative #
[史上最详细Windows版本搭建安装React Native环境配置](http://www.lcode.org/%E5%8F%B2%E4%B8%8A%E6%9C%80%E8%AF%A6%E7%BB%86windows%E7%89%88%E6%9C%AC%E6%90%AD%E5%BB%BA%E5%AE%89%E8%A3%85react-native%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# kotlin #
[kotlin学习资源整理](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=401833091&idx=1&sn=9685218eeac4abfbafdfacd81950bfa1)
[Kotlin for android developers](https://github.com/wangjiegulu/kotlin-for-android-developers-zh/blob/master/SUMMARY.md)
[Building a Kotlin project 1/2](http://cirorizzo.net/2016/03/04/building-a-kotlin-project/?utm_source=Android+Weekly&utm_campaign=36def426b1-Android_Weekly_195&utm_medium=email&utm_term=0_4eb677ad19-36def426b1-337851685)
[Building a Kotlin project 2/2](http://www.cirorizzo.net/2016/03/04/building-a-kotlin-project-2/?utm_source=Android+Weekly&utm_campaign=36def426b1-Android_Weekly_195&utm_medium=email&utm_term=0_4eb677ad19-36def426b1-337851685)
[实战Kotlin@Andorid（二）：界面构建与扩展方法](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=403568637&idx=1&sn=e6edfa6ef2029e0f6c1892ed7d2611d2#rd)

# 简历 #
[程序员，你的简历应该这样弄](http://www.devstore.cn/essay/essayInfo/5557.html)


# 网站 #
[在线 API 文档、技术文档工具 ShowDoc  ](http://doc.star7th.com/index.php/)

# Java #
[ java提高篇（四）-----抽象类与接口](http://email.mail.gank.io/c/eJwVzrkOgzAQBNCvwaW1u14fFC6QIP9hbHMoHAHc5O_jSFO8qWaS5xiVMmL1BGiAQQOxVUoikWOJih1Io_th6HpuGPawbnIOx1uup1g8B5MhkYXWKoiEYM1Ik55ianWaAordI2LL5MTml1I-jeoaetWM2znL-KRDHrnUHpd8PM-3KtxljVuuSrnUuacKyWlHxorba0TDbN3_zXXJeO4_Pwc2vQ)
[线程、多线程与线程池总结](http://www.jianshu.com/p/b8197dd2934c)
[你离顶尖Java程序员，只差这11本书的距离](http://www.techug.com/distance)
[反射、注解与依赖注入总结](http://www.jianshu.com/p/24820bf3df5c)

# 内存优化 #
[Android内存优化之OOM](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2015/0920/3478.html)
[Android 内存泄漏总结](https://yq.aliyun.com/articles/3009)


# 产品 #
[产品经理信息收集渠道大盘点](http://www.devstore.cn/essay/essayInfo/6155.html)

TODO 新技术
1.kotlin
2.Reace Native
3.swift