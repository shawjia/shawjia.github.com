---
layout: post
title: "JavaScript 中的 label"
description: ""
category: 
tags: [JS]
---
{% include JB/setup %}

JavaScript 中的 label 是一个比较少用的特性，使用方式如下:

    labelname: statement

是的，label可以用在任意表达式前面，但一般而言，label 用在循环以及条件判断前面会更有用一点。在循环前面放置 label 时，可以使用 `break labelname` 来退出循环，也可以通过 `continue labelname` 跳过当前循环，直接执行下一次。

<script src="https://gist.github.com/2893204.js"> </script>

更多，请参考 **JavaScript: The Definitive Guide 5.6.1**。