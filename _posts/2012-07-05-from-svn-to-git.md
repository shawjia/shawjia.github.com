---
layout: post
title: "从 SVN 到 Git(如何搭建 Git 服务器)"
description: ""
category: 
tags: []
---
{% include JB/setup %}

## 版本库切换

前公司用的是 SVN，非常落后。来到新公司后，我搭建了一个 Git 服务器。

从 SVN 其实可以无缝切换到 Git 的，只是要做好一些准备。git-svn 工具是第一个需要的，它允许我们将 svn 版本库 clone 成一个 git 库。

`git svn clone svn://host/path/to/repo --no-metadata -A map`

使用`--no-metadata`参数返回的 commit 中不带 git-svn-id 的尾巴，`-A` 参数允许你映射 SVN 帐号，map 文件举例如下:

	svnname1 = gitname1 <name1@inc.com>
	svnname2 = gitname2 <name2@inc.com>

更多参数请参考 [git-svn 文档](http://git-scm.com/docs/git-svn)。

## 搭建 Git Server

使用 [gitolite](https://github.com/sitaramc/gitolite/) 就可以，非常简单…

