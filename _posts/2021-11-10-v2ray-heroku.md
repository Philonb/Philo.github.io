---
layout: post
title: 免费VPS(Heroku)申请，自搭v2ray科学上网
categories: 科学上网
description: 申请免费的VPS，自搭v2ray翻墙
keywords: 科学上网，Heroku 
---

# 利用Heroku免费vps自搭v2ray科学上网

  自从开始使用github后，我就一直在找各种科学上网的方法。这次就学会了在Heroku免费申请vps。

  因为本人在自搭v2ray之前就有各种免费的vpn，所以一直不舍得花钱在vultr买vps。本来先盯上了甲骨文，然后申请到一半要添加付款方式，必须要使用万事达卡或者visa之类的银行卡。在微信上在线申请时未满18不能申请。所以最后看上了Heroku，这个只需要邮箱就可以。

## 1,准备工作:下载v2ray，熟悉一下v2ray的使用

我用阿里云盘分享了「v2rayN.jpg」，你可以不限速下载🚀 复制这段内容打开「阿里云盘」App 即可获取 链接：https://www.aliyundrive.com/s/kYFnU8nF4mA

  下载后将后缀.jpg删除(不用加后缀.zip,只要删除)用解压器打开解压即可。

解压后打开文件夹，打开v2rayN.exe。(想要方便点就自己创建一个快捷方式放在桌面)

这是一个老版本的v2rayN，想要最新版的，点击检查更新把每一个更新一下就行。![](https://pic.imgdb.cn/item/618bd58d2ab3f51d910e967d.png)

我简单介绍一下快捷键 Ctrl p 测试服务器延迟，Ctrl t 测试服务器速度，delete删除服务器，Ctrl v 批量导入服务器URL。另外v2ray还支持扫描二维码导入服务器。

当我们成功导入了服务器时，按Ctrl p测试延迟，ctrl t测试速度，如果测ping是timeout，测速度是远程服务器返回错误，那么这个服务器就是不可用的。

## 2,在淘宝买一个谷歌Gmail邮箱账户

  Heroku注册不建议使用国内的邮箱，最好使用Gmail邮箱。谷歌账户注册不能使用中国的手机号码(这点真烦，我之前注册过好几次，都没成功)

  购买后客服应该会教更改更改邮箱密码之类的，这个就按照她说的做就行。既然要更改就要进入Gmail，很遗憾的是Gmail在中国是没法访问的，所以我们需要科学上网。但别急，因为恐怕heroku也是要科学上网才能进入的。所以我在步骤3准备了临时的免费vpn

## 3,使用microsoft edge扩展里的免费vpn科学上网或者扫我分享的v2ray节点

  打开edge，点击这个拼图样子的地方，点击查找新扩展

![](https://pic.imgdb.cn/item/618bda512ab3f51d911026ad.png)

![](https://pic.imgdb.cn/item/618bda902ab3f51d91103fb4.png)

![](https://pic.imgdb.cn/item/618bdb742ab3f51d9110918c.png)

(不得不说扩展真好用)

搜索setupvpn，点击安装。安装完成后可以看到扩展拼图左边多了个东西

![](https://pic.imgdb.cn/item/618bdbc72ab3f51d9110aea9.png)

![](https://pic.imgdb.cn/item/618bdc4c2ab3f51d9110e1a2.jpg)

点击一下，按照要求注册，验证邮箱后登录。选择免费服务器里的节点建议选俄罗斯，印度，新加坡(我最开始用的时候新加坡节点最快，但现在连接上都有点慢，并且速度也变慢了很多)

![](https://pic.imgdb.cn/item/618bdc912ab3f51d91110052.png)

这个是我在使用v2ray之前一直使用的一款免费vpn，是我在扩展里找到的为数不多的真的可以用的免费vpn。免费用户会限制一天流量(我以前拿来测试能不能看8K然后直接用完了一天的流量。当时新加坡节点能够稳定看4K)

----

![](https://pic.imgdb.cn/item/618be0a82ab3f51d91126911.png)

在v2rayN中按ctrl s(或者点击左上角服务器一栏点击扫描屏幕上的二维码)扫描屏幕上的二维码

成功导入后双击该服务器

![](https://pic.imgdb.cn/item/618be1592ab3f51d9112afba.png)

路径一栏如果不是/path/323127100515请修改为/path/323127100515

![](https://pic.imgdb.cn/item/618be1ae2ab3f51d9112d89a.png)

右击v2rayN,系统代理选择自动配置系统代理，服务器选择刚刚导入的服务器。然后就能科学上网了。

![image-20211110231452640](C:\Users\86138\AppData\Roaming\Typora\typora-user-images\image-20211110231452640.png)

----

如果上面两个都不行，还可以试试一个叫自由海的edge扩展程序，虽然不是免费的，但有三天试用期。

## 4,fork v2ray-heroku专案至自己的github仓库，按照要求修改，最后部署v2ray

首先在自己的github创建一个新的仓库，命名不能包含v2ray和heruko这样的关键字。初始化好后进入这个页面下载专案[bclswl0827/v2ray-heroku: 用于在 Heroku 上部署 V2Ray WebSocket。 (github.com)](https://github.com/bclswl0827/v2ray-heroku)

下载解压到自己的本地仓库然后上传到github仓库。如果下载很慢，也可以在我的阿里云盘下载(一样地删后缀,阿里云盘不让分享压缩包)

我用阿里云盘分享了「v2ray-heroku.jpg」，你可以不限速下载🚀 复制这段内容打开「阿里云盘」App 即可获取 链接：https://www.aliyundrive.com/s/PJtoKsi6mJZ

按照readme里的要求做好。

因为过量的使用会导致封号，所以即使速度可以看4K但也别有事没事非要看个4K，合理的使用是不会导致封号的。以及我们可以多开几个节点，别一直用一个，防止一个节点用的过多被系统判定为滥用而封号。

这次演示我也刚好开第二个节点。

![](https://pic.imgdb.cn/item/618bea032ab3f51d9115c627.png)

这是我新建的下载好专案的仓库，点击readme.md，右上角的这个笔一样的地方编辑，将19行我加荧光的地方改成自己的。比如我的就是[Philonb](https://github.com/Philonb)/**[myvps-2](https://github.com/Philonb/myvps-2)**

![](https://pic.imgdb.cn/item/618bea992ab3f51d911654d0.png)

![](https://pic.imgdb.cn/item/618beb062ab3f51d91172067.png)

保存后记得在本地仓库打一下git pull将线上仓库做的改变应用到本地仓库上。

---

点击heroku链接，先注册好账号(用Gmail注册),要在邮箱里点击验证然后继续进行密码设置。

注册好后我们重新点击heroku链接登录进入如此界面，app name自己打一个，例如:philovps2

注意首字母不能大写。其余什么都不要改，点击Deploy app。等待进程结束，点击manage app，然后就进入了个人页面。我们点击settings。

![](https://pic.imgdb.cn/item/618bec502ab3f51d9117e088.png)

![](https://pic.imgdb.cn/item/618becfa2ab3f51d91181a9c.png)

![](https://pic.imgdb.cn/item/618bed672ab3f51d91184d2d.png)

向下翻，找到domain一栏,复制一下网址。

![](https://pic.imgdb.cn/item/618bedd42ab3f51d911883bd.png)

## 5，在v2ray中添加刚刚建好的vps

点击服务器，添加VMess服务器，地址粘贴刚刚复制的网址同时去掉最前面的https://和最后一个/，端口打443，ID在heroku网页中。找到config vars一栏点击reveal config vars复制ID到v2ray中。额外ID不用和加密方式不用改，别名随你自己，比如我是第二个节点就命名为heroku 2。传输协议选择ws，伪装域名和类型都不用打，路径改成/。底层传输安全选择tls，跳过安全证书验证选择true。点击确定。

![](https://pic.imgdb.cn/item/618bee7c2ab3f51d9118c669.png)

![ ](https://pic.imgdb.cn/item/618bef492ab3f51d91191a52.png)

![](https://pic.imgdb.cn/item/618bef942ab3f51d91193a3d.png)

![](https://pic.imgdb.cn/item/618bf0d42ab3f51d91199d8b.png)

这个时候我们的v2ray就搭建好了，我们可以试一下测试ping值和速度。

![](https://pic.imgdb.cn/item/618bf1382ab3f51d9119bed0.png)

![](https://pic.imgdb.cn/item/618bf1cb2ab3f51d9119f8bb.png)

可以看到ping直接timeout，速度也为0。这个时候没法用

## 6，通过 CloudFlare Workers反向代理提速

[Cloudflare - Web Performance & Security](https://dash.cloudflare.com/login)

点击链接进入Cloudflare官网,我们继续使用Gmail注册。注册后登录。点击Workers

![](https://pic.imgdb.cn/item/618bf3a12ab3f51d911ac7f8.png)

初次使用需要创建子域，我们按照默认的一直点下一步就行。进入此等界面点击创建Workers,里面的脚本要改成下面的内容。

![](https://pic.imgdb.cn/item/618bf40e2ab3f51d911b02bc.png)

```java
addEventListener(
	"fetch",event => {
		let url=new URL(event.request.url);
		url.hostname="域名";
		let request=new Request(url,event.request);
		event. respondWith(
			fetch(request)
		)
	}
)
```

域名仍然是heroku里的那个网址,复制粘贴后删除前面的https://和最后的/。保存并部署，再点击发送，出现400bad就说明成功了



![](https://pic.imgdb.cn/item/618bf6b92ab3f51d911c5464.png)

复制一下这里的网址，双击v2ray中的服务器，将地址改为这个网址并去掉https://和末尾的/。

我测试了一下ping和速度，ping255ms，速度4.9M/S。

延迟还是较高。这是因为CloudFlare随机给我们的ip不是最佳ip

## 7,选择最佳ip

选择最佳ip要用到一个工具，进入下面的网址进行下载

[badafans/better-cloudflare-ip: 查找适合自己当前网络环境的优选cloudflare anycast IP (github.com)](https://github.com/badafans/better-cloudflare-ip)

有各种版本的，根据需要下载。我演示的是windows版本。

或者在我的阿里云盘下载windows版本的

我用阿里云盘分享了「选择最佳ipwindows.jpg」，你可以不限速下载🚀 复制这段内容打开「阿里云盘」App 即可获取 链接：https://www.aliyundrive.com/s/37ohHWBwavB

![](https://pic.imgdb.cn/item/618bf9042ab3f51d911d50fa.png)

打开CF优选ip，会让我们选择需要的带宽。建议不要选太大，太大的话根本选不到这么高带宽的ip。所以可以保守点选择50Mbps，觉得不够也可以选100Mbps。输入后等待最佳ip筛选出来。

上次我选的是50Mbps,这次我选择的是100Mbps。两次最终选出来的确是远远大于50和100的。只比我实际带宽小一点

![](https://pic.imgdb.cn/item/618c75e92ab3f51d9140f77c.png)

打开v2ray，双击刚刚建好的vps。复制地址一栏粘贴至伪装域名一栏。然后我们复制优选ip粘贴到地址，点击确定。

![](https://pic.imgdb.cn/item/618c76df2ab3f51d91415aa1.png)

我们接着测一下ping值和速度，可以看到我的两个节点都只有三十多ms的延迟，速度也还行而且相较于我上面的节点速度更加稳定

![](https://pic.imgdb.cn/item/618c77222ab3f51d914173fa.png)

![](https://pic.imgdb.cn/item/618c77d12ab3f51d9141bd7a.png)

## 8,右键任务栏的v2ray，系统代理选择自动配置系统代理，服务器选择刚建好的vps

当想要访问外网时就在系统代理里选择自动配置系统代理，访问内网时就清除系统代理。
