title: Android自定义控件学习
date: 2015-09-24 14:36:18
tags: android
categories: android

---
# 控件架构 #
控件分为ViewGroup控件与View控件。ViewGroup控件作为父控件可以包含多个View控件，并管理包含的View控件。通过ViewGroup,整个界面上的控件形成了一个树形结构，这也就是我们常说的控件树，上层控件负责下层子控件的测量与绘制，并传递交互事件。

# View的测量 #
