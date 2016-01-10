---
layout: post
title: git的基本使用
date: 2015-12-26
categories: blog
tags: [研发]
description: 终于要开始小白之旅啦。


---

>Date:2015-12-26  
>Updated:2016-01-10

git是代码管理工具，方便开发者之间的协作。现在在各个开发平台上都已经出现了git的可视化管理客户端，然而对于通过shell命令
对代码库进行管理永远比通过可视化界面上的操作来得稳妥，下面根据自身使用经验，就git的使用规范以及常见命令做入门介绍。

>使用规范：

  git branch feature_jchen master (在本地基于master分支创建feature_jchen分支)

  每次开发之前都需要更新自己本地的master分支，命令如下：
  
  git pull origin master
  然后，执行以下命令将mater分支合并到你正在开发的feature_xxx分支来保持代码最新。
  
  git checkout feature_jchen（切换当前分支到feature_jchen）
  
  git merge master（将master分支合并到feature_jchen分支）

  每个人在以自己名字缩写结尾的在feature_xxx分支下进行开发。
  
  git add . (加入新开发的功能)
  
  git commit (将新开发的功能提交到本地的feature_jchen分支)
  
  git push (将本地的feature_jchen分支推送至服务器上的origin/feature_jchen分支)
  
  建议不要直接在master分支上开发，由研发负责人执行以下命令将feature_jchen分支合并到master分支。
  
  git checkout master（切换当前分支到master）
  
  git merge feature_jchen（将feature_jchen分支合并到本地master分支）
  
  git push origin master（发布master分支）
 
>常见命令

- git clone git@github.com:username/username.github.com.git 从线上代码库拷贝远程代码到本地进行开发
- git add 添加修改到暂存区（本地）
- git commit 添加修改到当前分支（本地）
- git push 添加修改到同名分支（线上）
- git merge -m “ something to describe this commit “ dev (和并本地dev分支的修改给当前分支)

- git stash （save uncommitted changes）
- git stash list  （list stashed changes in this git）
- git stash pop （apply last stash and remove it from the list）
- git stash apply （恢复之前的工作记录，但是工作记录列表中并不移除）
- git stash drop (删除工作记录列表中的最新一条)
- git stash clear (删除所有工作记录)

- git log –-pretty=oneline （简要显示当前分支的commit记录）
- git log --stat (显示简要的增改行数统计,每次提交文件的变更统计)
- git checkout –b name (创建+切换分支)
- git branch –d name (删除分支)
- git reflog  获取版本号
- git reset –hard HEAD~100(回退到100个版本)
- git pull(更新本地分支的代码，与对线上代码的修改)
- git status（查看当前本地分支代码的状态）