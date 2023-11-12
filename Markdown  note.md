### 1.Markdown 标题语法

要创建标题，请在单词或短语前面添加井号 (`#`) 。`#` 的数量代表了标题的级别。如：



| `# Heading level 1`     | 一级标题 |
| ----------------------- | -------- |
| `## Heading level 2`    | 二级标题 |
| `### Heading level 3`   | 三级标题 |
| `#### Heading level 4`  | 四级标题 |
| `##### Heading level 5` | 五级标题 |
| `###### Heading level 6 | 六级标题 |



### 2.Markdown 段落

要创建段落，请使用空白行将一行或多行文本进行分隔。如：

#I really like using

***空一行**

#I really do not like using



### 3.Markdown 换行语法

在一行的末尾添加两个或多个空格，然后按回车键,即可创建一个换行，如：
#I really do not like using  *空格
#but it is necessary

此外，还可以使用HTML 的 `<br>` 标签来实现换行。

### 4.Markdown 强调语法

###### (1)粗体

要加粗文本，请在单词或短语的前后各添加**两个星号**或**下划线**，如需加粗一个单词或短语的中间部分用以表示强调的话，请在要加粗部分的两侧各添加两个星号。如：

| Markdown                     | 结果                       |
| ---------------------------- | -------------------------- |
| `I just love **bold text**.` | I just love **bold text**. |
| `I just love __bold text__.` | I just love **bold text**. |
| `Love**is**bold`             | Love**is**bold             |





###### （2）斜体

要用斜体显示文本，请在单词或短语前后添加一个**星号**或**下划线**。要斜体突出单词的中间部分，请在字母前后各添加一个星号，中间不要带空格。

| markdown                               | 结果                                 |
| -------------------------------------- | ------------------------------------ |
| `Italicized text is the *cat's meow*.` | Italicized text is the *cat’s meow*. |
| `Italicized text is the _cat's meow_.` | Italicized text is the *cat’s meow*. |
| `A*cat*meow`                           | A*cat*meow                           |



### 5.Markdown 引用语法

要创建块引用，请在段落前添加一个 `>` 符号。如：

```
> Dorothy followed her through many of the beautiful rooms in her castle.
```

#### 嵌套块引用

块引用可以嵌套。在要嵌套的段落前添加一个 `>>` 符号。如：

```text
> Dorothy followed her through many of the beautiful rooms in her castle.
>
>> The Witch bade her clean the pots and kettles and sweep the floor and keep the fire fed with wood.
```



### 6.Markdown 列表语法

#### 有序列表

要创建有序列表，请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。如：

1. First item

2. Second item

3. Third item

4. Fourth item

   

#### 无序列表

要创建无序列表，请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。如：

##\- First item
\- Second item
\- Third item
\- Fourth item

\##* First item
\* Second item
\* Third item
\* Fourth item

\##- First item
\- Second item
\- Third item
  \- Indented item
  \- Indented item
\- Fourth item



### 7.Markdown 代码语法

要将单词或短语表示为代码，请将其包裹在反引号 ( ` ) 中。如：

| Markdown                              | 结果                                |
| ------------------------------------- | ----------------------------------- |
| `At the command prompt, type `nano`.` | At the command prompt, type `nano`. |

#### 转义反引号

如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号(````)中。

| Markdown                                | 结果                                |
| --------------------------------------- | ----------------------------------- |
| ```Use `code` in your Markdown file.``` | `Use `code` in your Markdown file.` |

#### 代码块

要创建代码块，请将代码块的每一行缩进至少四个空格或一个制表符。如：

```text
   <html>
      <head>
      </head>
    </html>
```



### 8.Markdown 分隔线语法

要创建分隔线，请在单独一行上使用三个或多个星号 (`***`)、破折号 (`---`) 或下划线 (`___`) ，并且不能包含其他内容。

```text
***

---

_________________
```



### 9.Markdown 链接语法



链接文本放在中括号内，链接地址放在后面的括号中，链接title可选。

超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`

#### 网址和Email地址

使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

```tex
<https://markdown.com.cn>
<fake@example.com>
```



### 10.Markdown 图片语法

要添加图像，请使用感叹号 (`!`), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。

插入图片Markdown语法代码：**！【图片】（图片链接”图片标题“）*

若要加链接，则应在其标题后面开一个（）加入





### 11.Markdown 转义字符语法



要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加反斜杠字符 \ 。

```text
\* Without the backslash, this would be a bullet in an unordered list.
```





#### 可做转义的字符

以下列出的字符都可以通过使用反斜杠字符从而达到转义目的。

| Character | Name                                                         |
| --------- | ------------------------------------------------------------ |
| \         | backslash                                                    |
| `         | backtick (see also [escaping backticks in code](https://markdown.com.cn/basic-syntax/escaping-characters.html#escaping-backticks)) |
| *         | asterisk                                                     |
| _         | underscore                                                   |
| { }       | curly braces                                                 |
| [ ]       | brackets                                                     |
| ( )       | parentheses                                                  |
| #         | pound sign                                                   |
| +         | plus sign                                                    |
| -         | minus sign (hyphen)                                          |
| .         | dot                                                          |
| !         | exclamation mark                                             |
| \|        | pipe (see also [escaping pipe in tables](https://markdown.com.cn/extended-syntax/escaping-pipe-characters-in-tables.html)) |
