# 使用 Markdown 快速记录

你是否遇到过以下场景？
- 使用Word写一篇文档，时不时需要让手离开键盘，用鼠标点击设置各种字体、段落格式，导致思路常常被打断
- 文章中插入一张图片（特别是长图片），由于当前页空间不足，图片被排到了下一页，给本页留下了巨大的空白
- 使用Word编辑好的文档，在另一台电脑上用WPS打开，格式完全乱了

或许你可以尝试一下Markdown

## 什么是Markdown？

Markdown是一种轻量级文本标记**语言**，用于实现快速简单的排版

看到“语言”二字，你可能会：
- 疑惑，排版还有专门的语言吗？
- 产生自然的抵触心理，拜托，我学个C语言就头疼得要死了，现在连写个文档都要我学语言

但你先别急，正因为Markdown是一种**语言**，才能实现**精准**地随心所欲地编辑，你能很清楚地知道每一个操作会产生什么效果；正因为Markdown是**轻量级**的语言，你才能很快上手学会使用

你可以在文本编辑器（推荐VSCode）或专用的Markdown编辑器（推荐Typora）中编写Markdown文档

## Markdown的特点及使用场景

### 特点

- 精准且优雅
  - Markdown可以以纯文本形式编辑，你再也不会被鼠标打断写作思路了
  - 麻雀虽小五脏俱全，语法覆盖了几乎所有常用排版功能，每种排版都有唯一对应的语法，而非散落在某个三级菜单的某个角落里的选项
  - 语法简单易读，比其他文本标记语言（如HTML）更适合编辑
  - 即使没有Markdown编辑器也能当txt正常阅读
- 更符合屏幕的排版和阅读习惯
  - 之前提到的分页问题，现在很多文档从写出来到完成它的使命，整个过程都是电子档，从不需要打印，但却和传统纸质文档一样分页，Markdown不分页的流式排版更符合屏幕的阅读习惯
- 格式与样式分离
  - Markdown只是规定了格式，但具体的参数如字体、字号、行距等都是由样式决定的
  - 假使你在维护一个文档库，需要使所有文档的风格统一，那么你只需要给所有文档使用同一个样式就可以了，日后要升级样式，也只需更改样式文件，而非对每一个文档做更改
- 便于版本管理
  - 因为Markdown是纯文本，所以可以使用git等工具轻松地进行版本管理，方便查看每一次的修改
- 标准开放且统一
  - Markdown的语法标准是开放的，任何人都可以根据这套标准实现自己的Markdown编辑器，这些编辑器对同一份文档的显示效果也都是相同的
  - Word的格式标准是微软公司的知识产权，只有Word能对其进行完美编辑，其他编辑器实现的都是部分特性或实现不标准，因此并不互通。并且如果某一天微软不再维护Word，之前用Word写的文档就处于一种非常尴尬的境地

### 适用场景

因为Markdown有上述特性，它适用于：
- 个人博客
- 学习笔记
- 开发文档
- `README   `说明文档

由于Markdown的功能有限，不适合编写一些比较正式的文档如论文、合同

这样的场景是不是只能用图形化的Word了呢？试试[$\LaTeX$](https://www.latex-project.org/)吧！

总之，Markdown的功能介于txt和Word之间，你可以把它看成带格式的txt

## 基本语法

### 标题

几级标题就在前面加几个`#`，为不破坏本文档的结构，下面示范4，5，6级标题：

```
#### 四级标题

##### 五级标题

###### 六级标题
```

#### 四级标题

##### 五级标题

###### 六级标题

### 段落与换行

在标准Markdown语法中，源文件空一行（或多行）表示文档段落，一行末尾有两个空格表示段内换行，注意源文件仅换行是不会换行的

```
这是一句话。
这句话不换行。  
这句话换行。

这是另一段话。
```

这是一句话。
这句话不换行。  
这句话换行。

这是另一段话。

### 加粗和斜体

用星号`*`包围的文字将斜体显示，用双星号`**`包围的文字将加粗显示，用三星号`***`包围的文字将同时斜体和加粗

```
请将*这里*斜体显示  
请将**这里**加粗显示  
请将***这里***加粗斜体显示  
```

请将*这里*斜体显示  
请将**这里**加粗显示  
请将***这里***加粗斜体显示  

### 列表

有序列表：

```
1. 第一点
2. 第二点
3. 第三点
```

1. 第一点
2. 第二点
3. 第三点

无序列表：

```
- 第一点
- 第二点
- 第三点
```

- 第一点
- 第二点
- 第三点

### 引用块和代码块

引用块和代码块内的文字将以特殊的格式显示，以满足特定需求（如采用等宽字体，代码高亮）

引用块的每一行前加上大于号`>`，引用可以嵌套

```
> 引用一段话
> 
> 引用另一段话
> 
>> 嵌套引用
```

> 引用一段话
> 
> 引用另一段话
> 
>> 嵌套引用

````
```
代码块使用反引号`包围，单个`为行内代码块，三个```为段代码块，本段文字写在段代码块中
段代码块可以在```后标明代码的语言，以便显示代码高亮
```

```python
if __name__=='__main__':
    print("Hello World")
```
````

```python
if __name__=='__main__':
    print("Hello World")
```

```
这是行内代码块的示例：`Markdown`代码块
```

这是行内代码块的示例：`Markdown`代码块

### 分割线

使用三个或以上的`-`，单独成段即可

```
---
```

---

### 链接

方括号`[]`后跟圆括号`()`，方括号内为链接标蓝的文字，圆括号内为链接地址

```
这是一个[链接](https://www.example.com)
```

这是一个[链接](https://www.example.com)

### 图片

和链接类似，只是在前面加一个`!`，方括号内为替代文本，圆括号内为图片地址，可以再附加说明，用双引号包围

```
![这是图片](./assets/Markdown.png "图片说明")
```

![这是图片](./assets/Markdown.png "图片说明")

## 扩展语法

### $\LaTeX$数学公式

和代码块类似，有行内公式和段公式，只是把反引号换成了`$`

$\LaTeX$具体语法请看[这里](./math_latex/)

```
$$$
\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}
$$$
```

$$$
\begin{aligned}
\dot{x} & = \sigma(y-x) \\
\dot{y} & = \rho x - y - xz \\
\dot{z} & = -\beta z + xy
\end{aligned}
$$$