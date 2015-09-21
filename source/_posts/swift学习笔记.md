title: swift学习笔记
date: 2015-09-20 07:56:48
tags:
categories: ios

---
<!--more-->
# 语法基础
## 可选类型(Optional)拆包和绑定
### nil
  使用可选类型来处理值可能缺失的情况
  
```
var num = "123"
var convertnum:Int? = num.toInt()
```
注意 nil 不能用于非可选的常量和亦是。如果你的代码有常量或者变量需要处理值缺失的问题，请把它们声明成对应的可选类型。

### if语句以及强制解析
```
var num = "123"
var convertnum:Int? = num.toInt()
if convertnum != nil {
 println("\(convertnum!)")
}
```
当你确定可选类型确实包含值之后，可以在可选的名字后面加一个!来获取值。这叫强制解析。

注意 使用!来获取一个不存在的可选值会导致运行时的错误，使用!来强制解析值之前，一定要确定可选包含一个非nil的值。

### 可选绑定
使用可选绑定来判断可选类型是否包含值，如果包含值就把值赋给一个常量或变量。可选绑定可以用在if和while语句中对可选类型的值进行判断并把值赋给一个常量或变量。

`if let b = convertnum {
 println("b=\(b)")
}`
 
 
如果转换成功，b常量可以在if语句中的第一个分支中使用。它已经被可选类型包含的值初始化过，所以不需要再使用!后缀来获取它的值。

###隐式解析可选类型
```
var num = "123"
var convertnum:Int! = num.toInt()
if convertnum != nil {
 println("\(convertnum)")
}
```
把想要用作可选类型的后面的？改成感叹号来声明一个隐式解析可选类型。

###断言
断言会在运行时判断一个逻辑条件是否为true。

```
let age = -3
assert(age >= 0,"A person age cannot be less than zero")
```
在这个例子中，只有age 》=0为true时，即age的值不为负的时候，代码才会继续招待。如果为负，断言被触发，终止应用。