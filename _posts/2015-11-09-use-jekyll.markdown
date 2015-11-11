---
layout:     post
title:      "学习jekyll编写blog之语言"
subtitle:   "markdown入门"
date:   2015-11-09
author:     "Simon"
header-img: "img/home-bg.jpg"
---

## 简介

markdown是github发布页面，以及jekyll下编写blog的主要语言。语法介绍如后文所述。

## 块元素

### 标题

* 使用“＝”或者“－”

	* “＝”定义h1字号的标题：

			这是一个H1
			=========

	* “－”定义h2字号的标题：

			这是一个H2
			---------

* 使用“＃”来定义标题等级。

		# h1的字号
		## h2的字号
		### h3的字号
		#### h4的字号
		##### h5的字号
		###### h6的字号

* 为了可读性，可以采取封闭的“＃”方式来定义标题

		# 这是个H1 #

		## 这是个H2 ###

		### 这是个H3 ######

### 引文

引文使用“>”来定义引文的开始，并且引文内可以使用其他md的关键标签。

	> ## 我是华丽的第一行
	>
	> 1. 第一行
	> 2. 第二行
	>
	> > 第三行
	> > 第四行
	>
	> 一行到底可以懒一点。懒一点。

### 列表

列表是使用“＊”和“＃”作为开始定义的，其内部可以使用其他md的关键标签。它主要分为无序列表和有序列表两种类型。

* 无序列表：

		* 第一行
		* 第二行
		* 第三行

		+ 第一行
		+ 第二行
		+ 第三行

		- 第一行
		- 第二行
		- 第三行

* 有序列表：

		1. 第一行
		2. 第二行
		3. 第三行

	
### 代码块

代码块是使用比正文段落多处4个空格或者1个制表符作为开始的。比如：

	这是个代码段落
	<?php
		$a = 1;
		$b = 1;
		echo $a+$b;
	?>
	
当缩进恢复的时候，格式也恢复到正文的格式。

### 水平线

想要画出水平线，很简单，如下4种写法任一即可：

	* * *

	***

	******

	- - - 

## 行元素

### 链接

直接看个代码例子

	访问[百度](http://www.baidu.com)

从例子上可见中括号中的是链接的展示名字，小括号中的是链接的地址。ps：小括号里的名字也可以是相对路径，如下：

	访问[BLOCK ELEMENTS](#section-6)

也可以通过序号来关联链接定义，如下：

	I get 10 times more traffic from [Google] [1] than from
	[Yahoo] [2] or [MSN] [3].

	[1]: http://google.com/        "Google"
	[2]: http://search.yahoo.com/  "Yahoo Search"
	[3]: http://search.msn.com/    "MSN Search"

### 强调

强调是通过将“＊”或者“_”放在需要强调的部分两侧来达到目的。示例如下：

	我需要*single asterisks*我需要

	强调 _single underscores_ 强调

如果需要字体加黑，则需要两个“＊”或者“_”。示例如下：

	**double asterisks**

	__double underscores__

### 代码标识

使用“｀”来完成对代码部分的标识。示例如下：

	请使用`array_merge()`函数

如果代码中包含“｀”则用如下方法解决：

	A backtick-delimited string in a code span: `` `foo` ``

	``There is a literal backtick (`) here.``

如果示html的tag，也使用“｀”进行标识。

	Please don't use any `<blink>` tags.

### 图片

图片和链接一样，但是需要增加“！”在行前。

	![haha1](http://img1.cache.netease.com/catchpic/3/3B/3B69F1C081FB9EA5A1850457683FD557.jpg)

------

掌握以上知识，对于markdown就有了初步的认识。我主要是将其应用于jekyll来编写我的blog。希望后续会为大家分享jekyll环境的搭建和使用。
	
