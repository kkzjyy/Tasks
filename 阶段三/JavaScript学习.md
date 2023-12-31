# JavaScript学习

## 1.基本概念

JavaScript 是互联网上最流行的脚本语言，这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。

JavaScript 是一种轻量级的编程语言，可插入 HTML 页面的编程代码

## 2.语法

JavaScript的语法和C语言类似，包括两条分语句之间使用分号，注释的方法，对大小写敏感但不同的是JavaScript中的变量需要使用 **var**来定义，如：

```
var a=100；//定义一个赋值为100的变量a
```

且对于变量的定义一般为字母开头，当然也可以使用 $ 和 _   但是不太常用。

此外，JavaScript没有任何的输出函数，一般通过以下方式输出数据：

- 使用 **window.alert()** 弹出警告框。

- 使用**prompt()**浏览器弹出输入框，用户可输入

- 使用 **console.log()** 写入到浏览器的控制台（给程序员看）

  按前两个输入，为：![image-20231123172018929](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123172018929.png)

![image-20231123172051664](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123172051664.png)

![image-20231123172107407](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123172107407.png)



## 3.**数据类型**

JavaScript中的数据类型有：字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）、对象(Object)、数组(Array)、函数(Function)

与C语言不同的是它的**赋值可以进行跨类型的赋值**，如：

```
var a=100；//此时a为数字
 var a= "hello"；  //此时a为字符串
```

如果你不确定，你可以用typeof来查看数据类型。

### 3.1字符串

字符串可以是引号中的**任意文本**。您可以使用单引号或双引号。

此外，在字符串内也可以再次使用引号，但不能与外面的引号重复。

```
var a="hello 'world'"
```

### 3.2数字

与C语言不同的是，JavaScript中的数字不会区分多种类型（如整型，浮点型），只分为数字一类。

```
var a=100；//此时a为数字
var a =100.0；//此时a仍为数字
```

### 3.3布尔

布尔（逻辑）只能有两个值：true 或 false，常用于测试语言中，与C类似

### 3.4数组

JavaScript创建数组有两种方式：1.数组字面量。2.用new Array（），如：

![image-20231123173102954](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123173102954.png)

以上两个数组是等价的。

注意：使用方法2时，如果只写一个数字，那么不会被认为时长度为1的数组。

![image-20231123173331960](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123173331960.png)

数组定义完后可以进行添加，一般使用push（）和unshift（）不同的时push是在数组后面添加，unshift是在数组前面添加。如：

![image-20231123193638940](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123193638940.png)

![image-20231123193652001](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123193652001.png)

与之相对的删除数组元素分别为pop（）和shift（），分别对应最后一个元素的删除和第一个元素的删除。

同时可以注意到：**在JavaScript中不同类型的数据可以放入同一个数组中**

### 3.5对象

对象（Object）  是一组无序的相关属性和方法的集合，所有的事物都是对象，如：字符串，数字，数组，函数等

对象是由**属性**和**方法**组成的。

属性：事物的**特征**，在对象中用**属性**来表示。

方法：事物的**行为**，在对象中用**方法**来表示

对象可以将数据更加直观的表示出来。

#### （1）字面量创建对象

花括号里包含表达这个事物的属性和方法，基本格式如下：

```
var obj ={属性名：值，属性名：值 ....}
```

如：![image-20231123200335089](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123200335089.png)

#### (2)new object创建对象

![image-20231123201010726](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123201010726.png)

#### （3）函数构造对象

首先我们得了解如何构造函数，构造函数基本格式：

```
function 构造函数名（）{
this.属性=值；
this.属性=值
......
}
```

![image-20231123203515303](JavaScript%E5%AD%A6%E4%B9%A0.assets/image-20231123203515303.png)

## 4.HTML/CSS/javascript三者的关系

HTML：写的是网页的主体框架，搭建的是一个基础的架构

CSS：是在HTML构造的架构基础上对网页的布局进行整理和上色，让网页布局更美观；

JavaScript：是对网页进行设计，让网页能够进行交互，不是单纯的“呆子”。