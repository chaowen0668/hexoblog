title: studio使用技巧
date: 2016-05-24 11:26:06
tags:
categories: android

---

## 注释 ##
File->Settings，搜索Templates，找到File and Code Templates，右边面板，Files->Class，然后修改编辑框里的内容。下面是接口(Interface)的注释模板。我的注释模板如下：
```
#if (${PACKAGE_NAME} && ${PACKAGE_NAME} != "")package ${PACKAGE_NAME};#end  
  
/** 
 * User: wuchaowen(511644784@qq.com) 
 * Date: ${YEAR}-${MONTH}-${DAY} 
 * Time: ${HOUR}:${MINUTE} 
 * FIXME 
 */  
public class ${NAME} {  
}  
```

## 成员变量前缀 ##
如果你命名成员变量习惯前面加一个m的前缀，但是生成getter和setter的时候，又不希望方法名中有这个m，可以如下设置。
File->Settings->Code Style->Java,然后在右边面板中选择Code Generation标签，Naming，Field这一行，对应的Name prefix中加上m.

## 快捷键 ##
http://seniorzhai.github.io/2015/02/05/AndroidStudio%E5%BF%AB%E6%8D%B7%E9%94%AE%E6%B1%87%E6%80%BB/



1. Ctrl(Command)+Alt(Option)+L	格式化代码
2. 添加 tools 命名空间。只需输入 toolsNS 然后按下 TAB 键。

