title: swift学习笔记
date: 2015-09-20 07:56:48
tags:
categories: ios

---
我的学习swift历程
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

### 隐式解析可选类型
```
var num = "123"
var convertnum:Int! = num.toInt()
if convertnum != nil {
 println("\(convertnum)")
}
```
把想要用作可选类型的后面的？改成感叹号来声明一个隐式解析可选类型。

### 断言
断言会在运行时判断一个逻辑条件是否为true。

```
let age = -3
assert(age >= 0,"A person age cannot be less than zero")
```
在这个例子中，只有age 》=0为true时，即age的值不为负的时候，代码才会继续招待。如果为负，断言被触发，终止应用。

# 字符串 #
## 字符串字面量 ##
 字符串字面量可以用于为常量和变量提供初始值
```
let someString = "Some string literal value"
```
## 初始化空字符串 ##
要创建一个空字符串作为初始值，可以将空的字符串字面量赋值给变量，也可以初始化一个新的String实例：
```
var emptyString = ""               // 空字符串字面量
var anotherEmptyString = String()  // 初始化方法
// 两个字符串均为空并等价。
```
您可以通过检查其`Boolean`类型的`isEmpty`属性来判断该字符串是否为空：
```
if emptyString.isEmpty {
    print("Nothing to see here")
}
// 打印输出："Nothing to see here"
```
## 字符串可变性 ##
您可以通过将一个特定字符串分配给一个变量来对其进行修改，或者分配给一个常量来保证其不会被修改：
```
var variableString = "Horse"
variableString += " and carriage"
// variableString 现在为 "Horse and carriage"

let constantString = "Highlander"
constantString += " and another Highlander"
// 这会报告一个编译错误 (compile-time error) - 常量字符串不可以被修改。
```
## 字符串是值类型 ##
Swift 的String类型是值类型。 如果您创建了一个新的字符串，那么当其进行常量、变量赋值操作，或在函数/方法中传递时，会进行值拷贝。 任何情况下，都会对已有字符串值创建新副本，并对该新副本进行传递或赋值操作。 值类型在 结构体和枚举是值类型 中进行了详细描述。

## 使用字符 ##
您可通过`for-in`循环来遍历字符串中的`characters`属性来获取每一个字符的值：
```
for character in "Dog!🐶".characters {
    print(character)
}
// D
// o
// g
// !
// 🐶
```
## 连接字符串和字符 ##
字符串可以通过加法运算符（+）相加在一起（或称“连接”）创建一个新的字符串：
```
let string1 = "hello"
let string2 = " there"
var welcome = string1 + string2
// welcome 现在等于 "hello there"
```

您也可以通过加法赋值运算符 (+=) 将一个字符串添加到一个已经存在字符串变量上：
```
var instruction = "look over"
instruction += string2
// instruction 现在等于 "look over there"
```

您可以用append()方法将一个字符附加到一个字符串变量的尾部：
```
let exclamationMark: Character = "!"
welcome.append(exclamationMark)
// welcome 现在等于 "hello there!"
```
## 字符串插值 ##
字符串插值是一种构建新字符串的方式，可以在其中包含常量、变量、字面量和表达式。 您插入的字符串字面量的每一项都在以反斜线为前缀的圆括号中：
```
let multiplier = 3
let message = "\(multiplier) times 2.5 is \(Double(multiplier) * 2.5)"
// message is "3 times 2.5 is 7.5"
```
## 字符串索引 ##
## 插入和删除 ##
## 比较字符串 ##
