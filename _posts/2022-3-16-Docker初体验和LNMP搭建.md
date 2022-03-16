---
layout: post
title: "Docker初体验和LNMP的搭建"
categories: Docker LNMP
description: 在腾讯云实验室进行的Docker初次学习，并按照步骤搭建了LNMP环境
keywords: Docker,LNMP,腾讯云实验室
---

## Docker实验

在腾讯云实验室进行了通过docker搭建好LNMP的教程，如果只是顺着手册步骤cv一遍，那么基本上记不住什么东西，而且理解也很浅。所以写一篇博客确实是可以巩固所学习的内容，以后有所遗忘也能够到博客看一看。

### Docker的安装

![腾讯云实验](https://pic.imgdb.cn/item/6231493f5baa1a80ababa54a.png)

mkdir 命令我还是很熟了，用来创建文件夹。但~/我却从来都没用过，不知道什么意思。上网查询得知其等效于 home/用户名。sudo命令是使用root权限进行这项命令，安装东西一般都要root权限。如果本身已经使用sudo su进入了root模式，那么其它命令前面就不用打sudo。我经常使用apt安装软件，不常用apt-get。实际上我也不清楚apt-get是什么，以前我有搜索过，但又不记得了。apt在我的理解里像是软件商店，ubuntu的默认软件商店是apt，centos的默认软件商店是yum。这个 -y 我只知道是某个附加的选项，但我不知道是什么意思，也许是安装最新版的意思。上网查询原来是yes的意思，很简单的用法。很多软件安装时都会问是否安装该软件(y n),加-y就不会再问了，直接安装

所以这一段的命令意思是 创建一个docker文件夹，进入docker文件夹，在此文件夹内安装docker的核心文件



![image-20220316104131509](https://pic.imgdb.cn/item/62314e8a5baa1a80abadd17a.png)

  **从网上摘的笔记**

### 更换镜像源

![](https://pic.imgdb.cn/item/623150075baa1a80abaebed9.png)

Docker的工作基础是镜像，镜像是啥之前我是完全不懂。但做上次作业体验了一下进入Docker镜像，感觉跟虚拟机很像，镜像和我实际的系统互不干扰，我在镜像中新建的东西不会出现在我的系统中。国内访问Docker Hub很慢，所以需要更换为国内的镜像源地址。

我曾经做过cat的笔记，最基本用法就是查看文件内容，我只会这个用法，其他用法都没掌握。

但是这个地方还是可以理解的。

新建或者只是打开写入(我不知道这里是哪种情况，也不知道cat能不能新建文件) /etc/docker/damon.json下面大括号里的内容，注册镜像:要替换的国内镜像源地址，打EOF表示退出写入。然后重启docker，退出root。

![](https://pic.imgdb.cn/item/623153de5baa1a80abb16953.png)

  **我的笔记**

### 下载需要用到的Docker镜像

![](https://pic.imgdb.cn/item/6231540e5baa1a80abb18aca.png)

Docker使用docker pull <镜像>来完成镜像的下载工作，这个用法与git一致，git push将本地文件夹上传至网络仓库，git pull将网络仓库内文件下载至本地文件夹。我们一般说的LNMP指的就是Linux,Nginx,mySQL,PHP。腾讯的这个实验使用了PostgreSQL代替mySQL。sudo docker image ls查看已下载的镜像。
