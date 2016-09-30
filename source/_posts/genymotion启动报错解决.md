title: genymotion启动报错解决
date: 2016-09-30 11:43:09
tags:
categories: 工具

---

今天发现启动genymotion报错，启动不了，以前也没问题的。
记录一下这过程。首先在virtualbox启动是报以下的错，
![](http://i.imgur.com/qcurTXw.png)

这也是错误的一段代码。

返回 代码:E_FAIL (0x80004005)
组件:MachineWrap
界面:IMachine {f30138d4-e5ea-4b3a-8858-a059de4c93fd}

google了一翻

1. 试过设置网卡，失败。
2. 重装过新版，失败

最后看到网上有人说使用旧版就可以了，我尝试下使用这个版本 [http://download.virtualbox.org/virtualbox/4.3.12/VirtualBox-4.3.12-93733-Win.exe](http://download.virtualbox.org/virtualbox/4.3.12/VirtualBox-4.3.12-93733-Win.exe "http://download.virtualbox.org/virtualbox/4.3.12/VirtualBox-4.3.12-93733-Win.exe")


成功了。为什么呢，搞不明白?  
