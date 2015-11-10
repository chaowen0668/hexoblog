title: Android自定义控件学习
date: 2015-09-24 14:36:18
tags: android
categories: android

---
# 控件架构 #
控件分为ViewGroup控件与View控件。ViewGroup控件作为父控件可以包含多个View控件，并管理包含的View控件。通过ViewGroup,整个界面上的控件形成了一个树形结构，这也就是我们常说的控件树，上层控件负责下层子控件的测量与绘制，并传递交互事件。

# 自定义View #
## 自定义view的分类 ##
1. 继承View重写onDraw方法

    这种方法主要用于实现一些不规则的效果,采用这种方式需要自己支持wrap_content,并且padding也要处理。

2. 继承ViewGroup派生特殊的Layout
   
    实现自定义布局。重新定义一种新的布局。需要处理View    

3. 继承特定的View(比如Textview)

    用于扩展已有的View的功能。不需要自己支持wrap_content和padding。
4. 继承特定的ViewGroup(比如LinearLayout)

   
## 自定义View的注意 ##
1. 让View支持wrap_content
2. 如果有必要，让你的view支持padding
3. 尽量不要在View中使用Handler。
4. View中如果有线程或者动画，需要及时停止。
5. View中带有滑动嵌套情形时,需要处理好滑动冲突。

## 自定义view示例 ##
### 继承View重写onDraw方法 ###

