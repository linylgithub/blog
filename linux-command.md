---
title: linux_command
date: 2018-02-12 16:31:42
tags:
---
#### 2018-02-12

##### sed

#匹配行前加

sed -i '/allow 361way.com/iallow www.361way.com' the.conf.file

#匹配行前后

sed -i '/allow 361way.com/aallow www.361way.com' the.conf.file

i: insert 前插入

a: append 后追加

而在书写的时候为方便区分，往往会在i和a后面加一个反斜杠：
    sed -i '/sourcesthing/i\addstring' file
    sed -i '/sourcesthing/a\addstring' file

# Linux最常用命令及快捷键

## 常用命令：

### 文件和目录

#### cd:

    # cd /home 进入'/home'目录
    # cd ..  返回上一级
    # cd ../../返回上两级目录
    # cd -  返回上次所在目录

#### cp: -a -d -f -i -p -r -l
    
    -d 复制时保留链接
    -f 覆盖已经存在的目标文件而不给出提示
    -i 与-f选项相反
    -p 除复制文件的内容外，还把修改时间和访问权限也复制到新文件中。
    -r 若给出的源文件是一个目录文件，此时将复制该目录下所有的子目录和文件。
    -l 不复制文件，只生成链接文件。

    # cp file1 file2 将file1复制为file2
    # cp -a dir1 dir2 复制dir1目录为dir2目录 --此选项通常在复制目录时使用，它保留链接、文件属性，并复制目录下的所有内容。其作用等于dpR参数组合。-a 等同于-dpr
    
#### ls:

    # ls 查看目录中的文件
    # ls -a 查看目录中的文件（包括隐藏文件）
    # ls -l 显示详细信息
    # ls -lrt 按时间显示文件（r表示反向排序，t表示按时间）

#### pwd:
    
    # pwd 显示工作路径
   
#### mkdir:

    # mkdir dir1 创建‘dir1’目录
    # mkdir dir1 dir2 同时创建两个目录
    # mkdir -p /tmp/dir1/dir2 创建一个目录树，即递归的创建创建目录

#### mv

    # mv dir1 dir2 移动/重命名一个目录

#### rm 
    
    # rm -f file1 删除 ‘file1’
    # rm -rf dir1 删除目录‘dir1’及其子目录

### 查看文件内容：

#### cat 

    # cat file1 从第一个字节开始正向查看文件的内容

#### head

    # head -2 file1 查看一个文件的前两行

#### more

    # more file1 查看一个长文件的内容

#### tac 
    # tac file1 从最后一行开始反向查看一个文件的内容

#### tail

    # tail -3 file1 查看一个文件的最后三行

### 文本处理

#### grep

    # grep str /tmp/test 在文件'/tmp/test'中查找“str”
    # grep ^str /tmp/test 在文件'/tmp/test'中查找以'str'开始的行
    # grep [0-9] /tmp/test 在文件'/tmp/test'中查找所以包含数字的行
    # grep -r str /tmp/* 在'/tmp'及其子目录中查找'str'

#### diff

    # diff file1 file2 找出两个文件的不同处
    # sdiff file1 file2 以对比的方式显示两个文件的不同




    

