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
[解决 singleTask onActivityResult() 无效的问题](http://mthli.github.io/singleTask-onActivityResult/)
[判断指定App是否位于前台的方法](https://github.com/wenmingvs/AndroidProcess)
[Android开发的那些坑和小技巧](http://www.cnblogs.com/lao-liang/p/4941653.html?f=tt&hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

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
[安卓下拉刷新开源库对比](https://github.com/desmond1121/Android-Ptr-Comparison/blob/master/README.md)
[Volley+OkHttp3+Gson（Jackson）开源库的封装过程](http://allenlin.leanote.com/post/volleyokhttpgson)
[如何更高效地使用 OkHttp](http://brucezz.github.io/articles/2016/02/21/effective-okhttp/)

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

# 提高 #
[深入理解Android之AOP](http://blog.csdn.net/innost/article/details/49387395)
[移动端图片格式调研](http://blog.ibireme.com/2015/11/02/mobile_image_benchmark/)
[如何选择 compileSdkVersion, minSdkVersion 和 targetSdkVersion](http://chinagdg.org/2016/01/picking-your-compilesdkversion-minsdkversion-targetsdkversion/)
[Android平台的崩溃捕获机制及实现](http://mp.weixin.qq.com/s?__biz=MzA4MzEwOTkyMQ==&mid=416184980&idx=1&sn=193b2a8aa3ac91fe54f647068c659633)
[携程Android App插件化和动态加载实践](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=401890966&idx=1&sn=b8d888acb7d4ace5d4e579a5588bf90b&scene=1&srcid=0219aSN6dGolDZQV0GnyqDPP&from=groupmessage&isappinstalled=0#wechat_redirect)
[Binder学习指南](http://weishu.me/2016/01/12/binder-index-for-newer/)
# 新特性 #
[Android M新特性Doze and App Standby模式详解](http://mp.weixin.qq.com/s?__biz=MzI1MTA1MzM2Nw==&mid=400185947&idx=1&sn=a591b76d2c9a085791fd4f12a5b31738&scene=2&srcid=11067beUUcVUcBRI1ajZZ2p7&from=timeline&isappinstalled=0&key=b410d3164f5f798e6f3fbdb81070f8443873c0d4632acc14a6513981556fa35169ba650e853f94945b244528cbd58799&ascene=0&uin=MTYzMjY2MTE1&devicetype=iMac+MacBookPro10%2C1+OSX+OSX+10.11.1+build(15B42)&version=11020201&pass_ticket=hgYTL4MW7%2FI9mnat%2BT9S2RRS0IkFfm6yOLSy%2F4bguL4%3D)
[聊一聊Android 6.0的运行时权限](http://droidyue.com/blog/2016/01/17/understanding-marshmallow-runtime-permission/)
[AppBar简述](http://www.jianshu.com/p/4ce0f3419ca8)
[AppBar的详解](https://github.com/SpikeKing/TestAppBar)
[Android 6.0: 动态权限管理的解决方案](http://www.jianshu.com/p/dbe4d37731e6)
[Android 6.0 运行时权限处理完全解析](http://blog.csdn.net/lmj623565791/article/details/50709663)
[Android Support Library 23.2有哪些新东西](http://www.jcodecraeer.com/a/anzhuokaifa/androidkaifa/2016/0226/3996.html)

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


# 开发工具 #
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



# 学习 #
[Android程序员 如何入门iOS ——故事从这里开始](http://segmentfault.com/a/1190000004268513)
[Android开发技术周报特刊之React Native](http://www.androidweekly.cn/android-dev-special-weekly-react-native/)
[生还是死？Android 进程优先级详解](http://chinagdg.org/2016/01/%E7%94%9F%E8%BF%98%E6%98%AF%E6%AD%BB%EF%BC%9Fandroid-%E8%BF%9B%E7%A8%8B%E4%BC%98%E5%85%88%E7%BA%A7%E8%AF%A6%E8%A7%A3/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)
[Kotlin for android developers》中文版翻译](https://github.com/wangjiegulu/kotlin-for-android-developers-zh)
[定期翻译Android官方博客](https://github.com/smallSohoSolo/android-developer-blog-cn)
[android学习资料](https://github.com/Freelander/Android_Data)
[10个很棒的学习Android 开发的网站](http://mp.weixin.qq.com/s?__biz=MzA4MTg4MjkzMw==&mid=214243534&idx=1&sn=7e8afe532c7809dc1b27456516d42239&scene=4#wechat_redirect)

# 数据库 #
[SQLite 大数据量 新增 / 修改 提升效率的办法](http://my.oschina.net/atearsan/blog/187226?fromerr=qCmwUhvO)
[使用replace](http://www.cnblogs.com/liping13599168/archive/2011/05/24/2054908.html)


# 安全 #
[Android应用安全开发之源码安全](http://drops.wooyun.org/mobile/12172)
[Android应用安全开发之防范无意识的数据泄露](http://drops.wooyun.org/mobile/12469)

# 测试 #
[测试技巧 – 你所不知道的测试黑科技](http://blog.chengdazhi.com/index.php/58)
[[团队分享]使用jenkins自动化构建android和ios应用](http://www.jayfeng.com/2015/10/22/%E4%BD%BF%E7%94%A8jenkins%E8%87%AA%E5%8A%A8%E5%8C%96%E6%9E%84%E5%BB%BAandroid%E5%92%8Cios%E5%BA%94%E7%94%A8/)
[世界级的Android测试开发流程（一）](http://blog.zhaiyifan.cn/2016/02/23/world-class-testing-development-pipeline-for-android-part-1/)
[世界级的Android测试开发流程（二）](http://blog.zhaiyifan.cn/2016/02/23/world-class-testing-development-pipeline-for-android-part-2/)

# sdk #
[sdk](https://www.sdk.cn/)


# 适配 #
[移动端适配方案(下)](https://github.com/riskers/blog/issues/18)

# 管理 #
[团队分享]如何更好的开发一个Android应用](http://www.jayfeng.com/2016/01/06/%E5%A6%82%E4%BD%95%E6%9B%B4%E5%A5%BD%E7%9A%84%E5%BC%80%E5%8F%91%E4%B8%80%E4%B8%AAAndroid%E5%BA%94%E7%94%A8/#more)


# Reactnative #
[史上最详细Windows版本搭建安装React Native环境配置](http://www.lcode.org/%E5%8F%B2%E4%B8%8A%E6%9C%80%E8%AF%A6%E7%BB%86windows%E7%89%88%E6%9C%AC%E6%90%AD%E5%BB%BA%E5%AE%89%E8%A3%85react-native%E7%8E%AF%E5%A2%83%E9%85%8D%E7%BD%AE/?hmsr=toutiao.io&utm_medium=toutiao.io&utm_source=toutiao.io)

# kotlin #
[kotlin学习资源整理](http://mp.weixin.qq.com/s?__biz=MzA3ODg4MDk0Ng==&mid=401833091&idx=1&sn=9685218eeac4abfbafdfacd81950bfa1)
[Kotlin for android developers](https://github.com/wangjiegulu/kotlin-for-android-developers-zh/blob/master/SUMMARY.md)
[Building a Kotlin project 1/2](http://cirorizzo.net/2016/03/04/building-a-kotlin-project/?utm_source=Android+Weekly&utm_campaign=36def426b1-Android_Weekly_195&utm_medium=email&utm_term=0_4eb677ad19-36def426b1-337851685)
[Building a Kotlin project 2/2](http://www.cirorizzo.net/2016/03/04/building-a-kotlin-project-2/?utm_source=Android+Weekly&utm_campaign=36def426b1-Android_Weekly_195&utm_medium=email&utm_term=0_4eb677ad19-36def426b1-337851685)

# 简历 #
[程序员，你的简历应该这样弄](http://www.devstore.cn/essay/essayInfo/5557.html)

TODO 新技术
1.kotlin
2.Reace Native
3.swift