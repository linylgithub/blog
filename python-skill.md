---
title: python技巧
date: 2018-02-11 16:17:05
tags:
---

## 1. 枚举 - enumerate

之前操作

    i = 0
    for item in iterable:
        print i, item
        i += 1

现在操作：
    
    for i,item in enumerate(iterable):
        print i, item

enumerate函数可以接收第二个参数。就像下面这样：
    
    >>> list(enumerate('abc'))
    [(0, 'a'), (1, 'b'), (2, 'c')]
    >>>
    >>> list(enumerate('abc',1))
    [(1, 'a'), (2, 'b'), (3, 'c')]

## 2. 字典/集合 生成

    >>> my_dict = {i: i * i for i in xrange(100)}
    >>> my_set = (i * 15 for i in xrange(100)}

### range 与 xrange区别：

xrange用法与range完全相同，所不同的是xrange生成的不是一个list对象，而是一个生成器
