---
layout: post
title: git的基本使用
date: 2015-12-26
categories: blog
tags: [web开发,git]
description: 终于要开始小白之旅啦。


---

>Date:2015-12-26  

git是代码管理工具，方便开发者之间的协作。下面根据自身使用经验，就git的使用规范以及常见命令做入门介绍。
>使用规范：

  git branch feature_jchen master (在本地基于master分支创建feature_jchen分支)

  每次开发之前都需要更新自己本地的master分支，命令如下：
  
  git pull origin master
  然后，执行以下命令将mater分支合并到你正在开发的feature_xxx分支来保保持代码最新。
  
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

git clone git@github.com:username/username.github.com.git //本地如果无远程代码

git pull 同步远程文件

git status 查看修改