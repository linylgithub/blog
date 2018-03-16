---
title: Python编码规范
date: 2018-03-16 18:46:48
tags:
---

## Python编码规范

本编码规范为PEP-8的精简版。

### 代码缩进

  1. 使用4个空格表示Python的缩进，不要使用Tab缩进，更不能混合使用Tab和空格。

### 空行

  1. Class和top-level的function的定义之间需要两行间隔；
  2. Class的method定义之间空一行；
  3. Function内逻辑无关段落之间空一行；
  4. 其他地方尽量不要再空行。

### 模块的Import

  1. Import的顺序：
    1. 标准模块，如os,sys
    2. 第三方模块
    3. 当前系统的模块

### 空格

总体原则，避免不必要的空格。
1. 右括号前不要加空格；
2. 逗号、冒号、分号前不要加空格；
3. 函数的左括号前不要加空格。如Func(1);
4. 序列的左括号前不要加空格。list[2];
5. 操作符左右各加一个空格，不要为了对其增加空格；
6. 函数默认参数使用的赋值符左右省略空格；
7. 不要将多句语句写在同一行；
8. if/for/while语句中，即使执行语句只有一句，也必须另起一行。

### 命名规范

  * CamelCase:[https://baike.baidu.com/item/camelCase/636859](https://baike.baidu.com/item/camelCase/636859)
  * snake_case:[https://en.wikipedia.org/wiki/Snake_case](https://en.wikipedia.org/wiki/Snake_case)

  1. 模块名采用全部小写的snake_case;
  2. Class的名采用UppuerCamelCase
  3. 自定义的异常命名规则为UpperCamelClassError的方式
  4. 模块内部变量和类的名前下划线
  5. 函数命名使用snake_case
  6. 常量使用全部大写的SNAKE_CASE
  7. Class的methods命名采用全部小写的snake_case
  8. 当methods名称和keyword冲突时，加一个下划线后缀
  9. Class的普通methods的第一个参数为self
  10. Class的Class methods的第一个参数为cls

  9.


