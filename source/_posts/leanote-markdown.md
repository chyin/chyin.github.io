---
title: Markdown常用基本操作（leanote与hexo中通用语法）
date: 2016-06-15 16:49:26
tags: leanote markdown
categories: 语法
---

## 段落、标题、区块引用
0. 一个段落是由一个以上的连接的行句组成，而一个以上的空行则会划分出不同的段落。
1. 标题，行首插入1到6个`#`,对应标题1到6阶。
2. 区块引用则使用‘`>`’角句号。

## 修饰和强调
1. 使用星号‘`*`’和底线‘`_`’来标记斜体。
2. 使用双星号‘`**`’表示粗体。
3. 使用双波浪线‘`~~`’表示横划线。

## 列表
1. 无序列表使用星号‘`*`’、加号‘`+`’和减号‘`-`’作为列表的项目标记。
2. 有序列表使用一般的数字接着一个英文句点作为项目标记（数字可以无序）。

## 链接
行内形式：直接在后面用括号接上链接。
> `[Chyin's blog](http://chyin.ac.cn 'website')`

> 输出为： [Chyin's blog](http://chyin.ac.cn 'website')

## 图片（与链接很像）
行内形式：（title是选择性的）：
> `![alt text](http://chyin.github.io/Gobang/maybe.PNG 'Title')`

> 输出为： ![alt text](http://chyin.github.io/Gobang/maybe.PNG 'Title')

## 代码
在一般的段落文字中，可使用反引号`` ``` ``来标记代码区段。或使用4个空格或一个tab进行缩进标记代码区段。

```python
class Employee:
   empCount = 0

   def __init__(self, name, salary):
        self.name = name
        self.salary = salary
        Employee.empCount += 1
```

## leanote中的其他语法

Markdown 扩展支持:

* 表格
* 定义型列表
* Html 标签
* 脚注
* todo list
* 目录
* 时序图与流程图
* MathJax 公式

详见 [Leanote Markdown语法手册](http://www.leanote.com/blog/post/531b263bdfeb2c0ea9000002)。

## 声明
关于Markdown的语法参考了[Markdown 语法说明](http://www.appinn.com/markdown/)， 其快速入门版本为[Markdwon: Basic](http://www.appinn.com/markdown/basic.html)。