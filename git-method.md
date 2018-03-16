---
title: git常用命令 
date: 2018-02-12 22:14:55
tags:
---

### 版本库初始化

创建文件夹，通过git init命令把这个目录变成Git可以管理的仓库：

    git init

忽略某些文件：在Git工作区的根目录下创建一个特殊的.gitignore文件，把需要忽略的文件名填进去，Git会自动忽略这些文件。

不需要从头写.gitignore文件，Github已经为我们准备各种配置文件，只需要组合一下就可以使用了。所有配置文件可以直接在线浏览：https://github.com/github/gitignore

增加文件：
    git add

    git commit

查看仓库当前状态：
    
    git status

查看修改内容：

    git diff

查看历史记录：

    git log

以便确定回到哪个版本

在git中，用HEAD表示当前版本，也就是最新的提交，上一个版本是HEAD^，上上一个版本是HEAD^^，HEAD~100。


版本回退：

    git reset --hard HEAD

    git reset --hard 3218811

Git提供了一个命令git reflog用来记录你的每一次命令,以便确定回到未来哪个版本
    
    git reflog


### 工作区

就是在电脑里能看到的目录

### 版本库

工作区有一个隐藏目录.git，这个不算工作区，而是Git的版本库

git add 把文件放到暂存区（stage）


撤销修改：

git checkout可以丢弃工作区的修改
    
    git checkout -- file

一种是自修改后还没有放到暂存区（版本库），一种是修改后添加到暂存区，又做了修改（回到添加到暂存区后的状态）
让该文件回到最近一次git commit或git add时的状态

删除文件：
    git rm
    git commit

### 远程仓库

git remote add origin git@github.com:linylgithub/learngit.git

git push -u origin master

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。

由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

每次本地提交后，只要有必要，就可以使用git push origin master推送最新修改；

从远程库克隆：
    git clone git@github,com:linylgithub/learngit.git

### 分支管理：

创建分支：
    
    git checkout -b dev

-b 表示创建并切换，相当于以下两条命令：
    
    git branch dev

    git checkout dev

用git branch 命令查看当前分支

切换回分支：
    
    git checkout master

将dev分支合并到master分支上：

    git merge dev

git merge命令用于合并指定分支到当前分支

删除分支

    git branch -d dev


