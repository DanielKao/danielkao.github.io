---
layout: post
title: "將某個branch的特定檔案merge到另一個branch"
date: 2014-01-22 11:03:26 +0800
comments: true
categories: GIT
---

##如何將某個Branch的特定檔案merge到另外一個Branch的同一個檔案？
```
git checkout A
git checkout --patch B f
```
	
其中, B不一定要是**branch**, 也可以是**commit**.

