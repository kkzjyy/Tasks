# HTML学习

## 1.概念

HTML指的是**超文本标记语言**(**Hyper Text Markup Language**)，他是一种用来描叙网页的语言.

如：运用HTML的图像标签可以把图片放入网页中，文字标签就可以把文字放入网页中。

超文本：

1.可以加入图片，声音等（超越了文本限制）

2.可以从连接多个主机上的文件（超链接文本）

## 2.语法与基本结构

### 2.1基本语法

HTML标签一般是由一对<>号包括的，如：<HTML>,同时，一般HTML标签是成对出现的，分为开始标签和结束标签，一般结束标签前面会有       “ / ”号。

```
<HTML>//开始标签，写在前面
</HTML>//结束标签，写在后面
```

注意：HTML中还存在单标签的情况，如：<br />

### 2.2标签关系

双标签有两种关系，分别是包含关系和并列关系。如：

```
<head>                         <head></head>             <title></title>                <title></title>//并列
</head>//此时<title>包含于<head>                             
```

### 2.3网页基本结构

对于一个网页来说，基本结构为：

```
<html>  //页面基础，一般称为根标签
  <head>  //网页头部 
    <title></title>//标题，包含在<head>中
  </head>
  <body>//网页的主体，内容
  </body>
</html>
```

## 3.常用标签

### 3.1文本标签

#### （1）标题标签

常见的标题标签为<h>,其为单词head的缩写，一共分为六个等级，重要性以此递减。需要注意的是，**每个标题都独占一行**。如：
![标题](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231121213221730-17005738853015.png)

#### （2）段落和换行标签

段落标签和换行标签分别为<p>和 <br />，在编写HTML时，在程序中的回车换行或者空格换行等在网页中均不会显示出来，必须要在文字前面和后面分别加上<p>和</p>才会被认为是一个段落，且与下一个段落中间空出一行 。如果你不想直接更换段落而只是单纯想换行，那<br />会是一个不错的选择。但要注意的是：   是单标签，一般用在要换行语句的前面。如：

![image-20231121215006302](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231121215006302.png)

得到的网页：

![image-20231121215139999](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231121215139999.png)

#### （3）文本格式化标签

常用的格式化标签有：

```
<i></i>//斜体   <em></em>//强调斜体
<b></b>//加粗    <strong></strong>//强调加粗
<del></del>//删除线
<ins></ins>//下划线
```

#### （4）区块标签

常用的有<div> 和<span >,通常作为一种容器，<div>定义了文档的区域，块级（一个独占一行），而<span>也是一个容器，但它的作用是将多个元素放在同一行，组合文档中的行内元素， 内联元素。如：

![image-20231122092911536](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231122092911536.png)

![image-20231122093006309](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231122093006309.png)







### 3.2表单标签

#### （1）基本组成：

表单由：表单域，表单控件（表单元素）和提示信息组成。

#### （2）表单域

表单域指的是一个包含表单元素的**区域**一般使用标签为<form>，<form>会把其区域内的信息提交给服务器。其基本形式如下：

```
<form action="服务器url地址" method="提交方式" name="表单名称">
各种表单元素控件
</form>
```

#### （3）表单元素

表单元素收集内容一般为<input>标签（input标签是一个单标签），input中可以有很多种属性，如：



|   属性    | 属性值  | 描述                      |
| :-------: | ------- | ------------------------- |
|   type    | 自定义  | 对输入形式的定义          |
|   name    | 自定义  | input元素的名称           |
|   value   | 自定义  | input元素的值             |
|  checked  | checked | input元素首次加载时就选中 |
| maxlength | 正整数  | 输入字段中字符的最大长度  |

**注意：type为必写属性**

其中type的属性值可以分为如下类型：

![image-20231122155155719](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231122155155719.png)

如要建立一个信息注册的网页：

![image-20231122160953227](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231122160953227.png)

结果为：![image-20231122161009745](HTML%E5%AD%A6%E4%B9%A0.assets/image-20231122161009745.png)

**注意：单选按钮和多选框一般有相同的name值，name和value一般是给后台人员观看**

