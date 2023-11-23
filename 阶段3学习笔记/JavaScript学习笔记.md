# JavaScript学习笔记

> 摸鱼禁止!!!!:sob:
>
> 这么跟C语言这么像呢？编程语言都是部分互通吗？

## 学习背景

+ 学习JavaScript基本语法
+ 了解JavaScript数据类型
  + 字符串（String）
  + 数字（Number）
  + 布尔（Boolean）
  + Null
  + Undefined
  + 对象（Object）
  + 数组（Array）
+ 了解HTML/`CSS`/JavaScript三者之间的关系 【重点】

## 目录

* JavaScript 简介
* JavaScript 学习
* HTML/`CSS`/JavaScript三者之间的关系

## 学习内容

### 1.JavaScript 简介

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。

JavaScript 是一种轻量级的编程语言。

JavaScript 是可插入 HTML 页面的编程代码。

JavaScript 插入 HTML 页面后，可由所有的现代浏览器执行。

JavaScript 很容易学习。

### 2.JavaScript 学习

#### 2.1 JavaScript语法

HTML 中的 Javascript 脚本代码必须位于**` <script>` **与 **`</script>`** 标签之间。

Javascript 脚本代码可被放置在 HTML 页面的 **`<body>`** 和 **`<head>`** 部分中。



可以把JavaScript直接**写在HTML文档**中:使用 document.write() 可以向文档写入内容。

**注意**：如果在文档已完成加载后执行 document.write，整个 HTML 页面将被**覆盖**。

也可以**写到控制台**：使用 **console.log()** 方法在浏览器中显示 JavaScript 值。

（需要使用浏览器调试模式，按F12打开调试后选择“Console”）



* **字面量**

在编程语言中，一般固定值称为字面量。共**数字（Number）字面量**、**字符串（String）字面量**、**表达式字面量**、**数组（Array）字面量**、**对象（Object）字面量**、**函数（Function）字面量**7种。

#### 2.2 JavaScript输出

JavaScript 没有任何打印或者输出的函数。可通过以下几种方式来输出数据：

- 使用 **window.alert()** 弹出警告框。
- 使用 **document.write()** 方法将内容写到 HTML 文档中。
- 使用 **innerHTML** 写入到 HTML 元素。
- 使用 **console.log()** 写入到浏览器的控制台。

#### 2.3 JavaScript 变量

在编程语言中，变量用于存储数据值。（C语言有讲）

JavaScript 使用关键字 **var** 来定义变量， 使用等号来为变量赋值，具体语法同c语言。

#### 2.4JavaScript 数据类型

**值类型(基本类型)**：字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）、Symbol。

**引用数据类型（对象类型）**：对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）。

JavaScript 拥有动态类型。这意味着相同的变量可用作不同的类型。可以使用 **typeof** 操作符来查看变量的数据类型。

##### 字符串

字符串是存储字符的变量。

字符串可以是引号中的任意文本。可以使用单引号或双引号，也可在字符串中使用引号，只要不冲突。

##### 数字

JavaScript 只有一种数字类型。数字可以带小数点，也可以不带。（比c语言那一大堆简洁多了:smile:）

极大或极小的数字可以通过科学（指数）计数法来书写.

##### 布尔（逻辑）

布尔（逻辑）只能有两个值：true 或 false。常用在条件测试中。

##### 数组

使用方法同c语言数组，var example=[]

##### 对象

由花括号分隔。在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义,属性间由逗号分隔。

空格和折行无关紧要。声明可横跨多行

##### Undefined 和 Null

Undefined 这个值表示变量不含有值。

可以通过将变量的值设置为 null 来清空变量。



**注意：声明新变量时，可以使用关键词 "new" 来声明其类型**

**JavaScript 变量均为对象。当您声明一个变量时，就创建了一个新的对象。**

### 3. HTML/`CSS`/JavaScript三者之间的关系

HTML、CSS、JavaScript，它们看上去是三种不同的技术，但在实际中却是相互搭配使用的:

* HTML是用来**标记内容**的（重在内容组织上）
* CSS是用来**修饰内容样式**的（重在内容样式美化展示上）
* JavaScript是用来**做交互**的

这三个搭配使用可以更好地编写网页。

但与此同时，HTML与CSS、JS也是不同的技术，是可以独立存在的。

HTML一般需要CSS和JS来配合使用，否则单一HTML文档无论是功能还是展示上效果都不理想；

CSS一般是不能脱离HTML或XML的，如果CSS脱离了HTML和XML，那就没有存在的必要的；

JS可以脱离HTML和CSS而独立存在；

JS可以操作HTML和CSS。

打一个形象的比方：如果把HTML比做**身体**，那CSS就好比是**衣服**，而JavaScript则意味着人能做的一些**高级动作**。





