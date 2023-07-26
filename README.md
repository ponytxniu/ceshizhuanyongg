---
title: '【腾讯云Cloud Studio实战训练营】使用Cloud Studio&Flutter完成跨平台博客的搭建'
subTitle: '使用Cloud Studio&Flutter完成跨平台博客的搭建'
summary: '本文我将使用Cloud Studio 以及Flutter完成自己的一个博客平台的搭建。并且会将该项目作为模版，供大家使用。'
tags: ['用户体验']
date: '2023-07-22'
author: '徐建国'
avatar: ![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-0.png)
description: Cloud Studio 是腾讯云自主研发的在线 IDE 集成开发环境。用户可以通过 Cloud Studio 创建项目的工作空间，进行在线编程、开发、调试等操作。Cloud Studio 还提供可分享的在线 IDE 开发环境功能。本文描述如何通过Cloud Studio&Flutter完成跨平台博客的搭建
keywords: 在线编程,WebIDE,CloudIDE,云端IDE,在线IDE,云端开发工具,在线集成开发环境,开发环境分享,代码托管,在线开发,在线调试,软件团队协作,CODING,Cloud Studio,Web IDE,Flutter,apk,流水线
---

# 前言

本文我将使用Cloud Studio 以及Flutter完成自己的一个博客平台的搭建。并且会将该项目作为模版，供大家使用。

先来看一下效果

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-1.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-2.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-3.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-4.png)


# 一.Cloud Studio 

Cloud Studio 是基于浏览器的集成式开发环境(IDE)，为开发者提供了一个永不间断的云端工作站。用户在使用CloudStudio 时无需安 装，随时随地打开浏览器就能在线编程。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-5.png)

大家也看到了，很多模版以及环境都有提供，大家也都知道我以前是搞Flutter的，于是就先尝试了一下Flutter模版，然后刚开始，可能确实不太会，但熟悉了一会，就发现他的好处了。

Cloud Studio 作为在线IDE，包含代码高亮、自动补全、Git集成、终端等IDE的基础功能，同时支持实时调试、插件扩展等，可以帮助开发者快速完成各种应用的开发、编译与部署工作。我将这次的这个博客网站使用Cloud Studio推送到了Gitee，[大家可以访问](https://gitee.com/jianguo888/flutter_bloc_super)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-6.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-7.png)


# 二.应用场景


Cloud Studio 在线编程工具适用于以下几个场景：

**2.1快速启动项目**

使用 Cloud Studio 的预置环境，您可以直接创建对应类型的工作空间，快速启动项目进入开发状态，无需进行繁琐的环境配置。

下面就是我的工作空间，大家可以下次使用的时候，进入对应的工作空间，就可以继续编写代码，很是方便。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-8.png)

**2.2实时调试网页**

Cloud Studio 内置预览插件，可以实时显示网页应用。当您的代码发生改变之后，预览窗口会自动刷新，这样您就可以在 Cloud Studio 内实时开发调试网页了。

下面这个就是我创建的第一个模版项目，你会发现很是方便。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-9.png)

**2.3远程访问云服务器**

Cloud Studio 支持您连接自己的云服务器，这样就可以在编辑器中查看云服务器上的文件，进行在线编程和部署工作。

只有有自己的云服务器，那么你就可以在这里通过配置，很方便的入手开发。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-10.png)


# 三.登录注册

Cloud Studio 在线编程平台支持使用[CODING (opens new window)](https://coding.net/?from_column=20420&from=20420)账号和 GitHub 账号，以及微信登录，可以在[登录 (opens new window)](https://cloudstudio.net/auth/realms/cloudstudio/protocol/openid-connect/auth?client_id=cloudstudio-apiserver&response_type=code&redirect_uri=https%3A%2F%2Foauth.cloudstudio.net%2Fapi%2Fpublic%2Foauth%2Fcallback%3Fsrc%3D%252F&team=&kc_idp_hint=)
界面输入相应的账号登录前往 Web IDE，这里我用的是微信登录。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-11.png)


# 四.工作空间的创建与使用

一个工作空间是一个虚拟计算单元，它包含独立的存储、计算资源以及开发环境。Cloud Studio 是以工作空间来组织的，本文为您介绍如何创建工作空间。

**4.1创建工作空间**

进入 Cloud Studio 云端 IDE，可以通过两种方式创建工作空间，**第一种方式**：点击模板直接创建工作空间，**第二种方式**：单击【新建工作空间】，进入工作空间创建页面

*4.1.1填写工作空间信息*

第一种方式点击模板创建工作空间，可自动生成工作空间名称，并运行模板的预置环境及样本代码。这里我用的是Flutter。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-12.png)

第二种方式，选择创建工作空间，然后选择预置环境，填写工作空间名、描述，并选择运行环境和代码来源。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-13.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-14.png)

-**工作空间名**：您的工作空间的唯一标识，只能由字母、数字、下划线（_）、中划线（-）、点（.）组成，不能包含空格或其它字符。


-**描述**：对该工作空间作用的描述。


-**运行环境**：工作空间内代码运行的环境，您可以选择预置环境，包含 Ubuntu、Python、Java 和 Node.js 四种；也可以选择将其连接到自己的云服务器上。


-**代码来源**：工作空间内的代码来源，此处我们选择“空”，即不添加任何代码。

单击【创建】按钮，即可完成工作空间的创建。您还可以创建代码来自于 Git 仓库的工作空间，代码会被自动克隆到工作空间


**4.2工作空间的使用**

您可以在 Cloud Studio 云端 IDE 的工作空间内存放自己的项目代码，安装所需要的软件环境，运行或编译项目，本文为您介绍如何使用工作空间。

注意：

-**数量限制**：目前每个用户最多可以创建 10 个工作空间，并且只能同时运行一个工作空间，如果您需要打开另一个工作空间需要先关闭当前运行中的工作空间。


-**时间限制**：每个用户每月可以免费使用工作空间共 1000 分钟，超出时间将产生扣费（连接云主机的工作空间无此限制）。


*4.2.1工作空间界面简介*

工作空间是我们主要的工作区域，主要由顶部菜单栏、左侧操作面板、右侧代码编辑区和底部状态栏组成。

您可以根据自己的习惯设置界面外观、偏好，安装自己需要的插件。

需要注意的是，您的**偏好设置和插件在每个工作空间中是互相隔离**的，也就是说您可以给不同的工作空间设置不同的偏好，安装不同的插件。这里面大部分和你在本地使用vscode是一样的。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-15.png)

我们可以通过终端来进行这些操作，点击菜单栏--终端--新终端，会在底部打开一个面板，点击【终端】切换到终端。

*4.2.2管理工作空间*


在 Cloud Studio 云端 IDE 的工作空间列表页面，您可以运行、停止、删除和恢复工作空间。


**运行**


单击对应的工作空间卡片，就会在新的页面打开并运行该空间，此时该工作空间卡片上会显示“运行中”状态。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-16.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-17.png)

**停止**


对于处在“运行中”状态的工作空间，单击卡片右边的【停止】，就可以停止运行该工作空间。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-18.png)

**删除**


您可以删除未运行的工作空间，单击工作空间卡片右下角的【删除】即可删除。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-19.png)

**恢复**


为了防止误删除，已删除的工作空间会展示在下方“已删除的工作空间”列表中，保留24小时。在此之前您可以随时单击【恢复】，还原您的工作空间，超过 24 小时未恢复的工作空间将被永远销毁。


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-20.png)

# 五.使用 Git 进行版本控制

**5.1Cloud Studio 查看SSH公钥**

这里我们点击个人头像，打开系统设置，里面有SSH公钥，然后我们把密钥复制，添加到Gitee


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-21.png)

**5.2Gitee添加SSH公钥**


在下图，添加SSH公钥，补充标题和公钥

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-22.png)

**5.3Gitee上新建一个仓库**

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-23.png)

在我们的云IDE的工作空间里，打开终端。


**5.4Cloud Studio配置邮箱和密码**

```shell
git config --global user.name "坚果"    
​
git config --global user.email "852851198@qq.com"                                                            
```

**5.5Cloud Studio提交代码**


然后初始化仓库，提交修改，添加commit信息，然后推送

```shell
​
git init
git remote add origin git@gitee.com:jianguo888/flutter_bloc_super.git
git add .
git commit -s -m '初始化'
git push origin master
​
```


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-24.png)


# 五.Flutter博客网站的开发

「**Flutter**」是谷歌的移动UI框架，Flutter 最近发布了 Flutter V3.10.6，可以快速在 「**iOS**」、「**Android**」、「**Web**」 等多平台上构建高质量的原生用户界面。 「**Flutter**」 可以与现有的代码一起工作。在全世界，「**Flutter**」 正在被越来越多的开发者和组织使用，并且 Flutter 是完全免费、开源的。 目前「**Cloud Studio 云端 IDE**」 支持 「**Flutter**」 Web 应用开发。这就是为什么今天我们使用在 Web、macOS 应用、Android 和 iOS 应用上运行的 flutter 创建响应式博客主题。 


**6.1创建项目**


打开云IDE之后，创建一个Flutter项目，当前，我使用的是 「**Flutter 3.0.1**」

创建完成之后，我们就可以编写代码

首先打开云IDE，选择创建项目

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-25.png)


然后这里我们给自己的项目命名

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-26.png)

等待项目加载完成

然后运行下面的这行命令

```shell
​
cd ./ && flutter pub get && flutter run -d web-server --web-port 9000  --web-hostname 0.0.0.0 && echo success
​
```

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-27.png)

我们可以选择打开内置浏览器或者浏览器

这里我选择打来浏览器，大家可以看到这个项目运行成功。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-28.png)

这个时候，说明我们的环境是ok的。我们可以后面的工作了

**6.2.打开端口面板实时预览调试**


点击最右边的按钮弹出预览页面。

看到这些红色的文字 To hot restart changes while running, press "r" or "R". 说明项目编译好了。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-29.png)

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-30.png)

修改代码重新编译

点击终端， 按 r 键即可重新编译， 再按预览页面的刷新按钮即可看到实时修改后的效果。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-31.png)

1.目前 Flutter Web 应用不支持热更新，需要手动刷新页面。
2.要项目编译完成才能代码预览页面， 否则会一直卡在 Loading 界面。
3.一直卡在 Loading 界面可尝试刷新预览界面。

**6.3发布web版**


我们希望你完成迁移后尽快将其发布，可以作为预览版：

 参考文章：  https://dart.cn/null-safety/migration-guide

细心的小伙伴可能会发现,安卓有android文件夹, iOS 有ios的文件夹,但目前目录结构是没有web文件夹的,

*6.3.1. 创建web文件夹*
输入下面的命令创建web文件

```shell
​
flutter create .
​
```

然后就会创建一系列web相关的文件 ,如下图, 目录结构也会多一个web的文件夹. 如下图

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-32.png)


*6.3.2. 打包web版本*


我们知道要给android手机用,需要打包apk出来, 要给iPhone手机用,需要打包ipa出来;同样的道理要给浏览器用,也需要打包web相关代码.

```shell
​
flutter build web --web-renderer html
​
flutter build web 
​
flutter build web --web-renderer canvaskit
​
```

这将生成包括资源的应用程序，并将文件放入项目的 「**/build/web**」目录中。

一般的应用程序的 release 版本具有以下结构：

content_copy

```shell
​
/build/web
  assets
    AssetManifest.json
    FontManifest.json
    NOTICES
    fonts
      MaterialIcons-Regular.ttf
      <other font files>
    <image files>
  index.html
  main.dart.js
  main.dart.js.map
```

启动 Web 服务器（例如，python -m SimpleHTTPServer 8000，或使用 [dhttpd](https://pub-web.flutter-io.cn/packages/dhttpd) package），然后打开 /build/web 目录。在浏览器中访问 localhost:8000（前文用 Python 启动的服务器）以查看应用程序的 release 版本。

经过测试,上面三种方式都可以打包web版本, 其中第一种是针对移动端的打包方式, 第二种是一般的打包方式, 第三种是针对pc端的打包方式.

那这3种方式打包出来,运行起来有什么不同呢

flutter build web --web-renderer html 打开速度最快,兼容性好(是指ie,chrome,safari等浏览器兼容)


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-33.png)


flutter build web 打开速度一般,兼容性好

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-34.png)


flutter build web --web-renderer canvaskit 打开速度最慢,兼容性好

*6.3.3结论*
 就是使用第一种打包方式会比较好
 
```shell
flutter build web --web-renderer html
```

**6.4常见问题**

-**坑1**:  找到了index.html,用浏览器打开一片空白
这个属于正常的, 这个不像前端web ,html css js那套,点击index.html就能访问的.  在flutter里面是不能直接访问的,一定要放到容器里面去才能访问,如:tomcat等

-**坑2**:  已经用nginx代理,用浏览器打开还是一片空白
那是因为文件路径引用不对.解决办法有2种  方法1:  用编辑器打开index.html,能看到源文件,把<base href="/">,改成<base href="">

方法2:  用编辑器打开index.html,能看到源文件,把<base href="/">,改成你服务器的路径比喻说:<base href="http://你的服务器ip:0-65536/web/">

然后nginx代理

```shell
  #flutter
    server {
       listen       251 ;
       server_name  flutterblog;
       location / {
           root   /root/study/flutter/web/;
           index  index.html index.htm;
        #    proxy_pass   http://127.0.0.1:12345;
        #    access_log  /usr/local/nginx/logs/go.101.log ;
​
       }
    }
​
```

# 七.自定义模板

自定义模板是 Cloud Studio 云端 IDE 推出的面向团队模板能力的功能。该功能支持将当前项目作为自定义模板，能够覆盖到 Git 仓库的项目、普通项目、示例项目等，很大程度上提高了团队标准化代码开发环境的一大诉求。

**7.1自定义模板功能简介**


当前自定义模板实现的功能主要有四个方面，创建、发布、分享和管理自定义模板。


**7.2创建自定义模板**


当您处在当前项目 IDE 中，您可以创建自定义模板：

这里我把我的Flutter 博客网站发布成模版。

（1）点击功能栏中的“文件”，在下拉选项中选择“发布自定义模板”；

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-35.png)

（2）右侧布局窗口中会自动打开新标签页，可以选择您心仪的图标和标签，以及填写您模板的描述


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-36.png)


点击完成


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-37.png)

**7.3发布自定义模板**


当您成功填写完自定义模板信息后，您可以进行自定义模板发布：

（1）点击“完成”即可发布您的自定义模板；

（2）在分享前点击“再次发布”，可以修改您的发布信息后再次分享，分享链接无变化，根据原模板已创建的 IDE 实例不受影响；



![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-38.png)


![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-39.png)


**7.4分享自定义模板**


当您的模板发布成功后，您可以有两种方式分享自定义模板：

（1）进入分享页，复制您的自定义模板链接，分享给您的伙伴；

坚果（个人）分享了「Flutter Blog」模板 https://cloudstudio.net/templates/r9IAX1JuTF2

（2）通过嵌入 Markdown 徽章进行分享，将模板徽章嵌入 README 文件或者博客中，您的伙伴点击徽章即可获取模板；

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-40.png)



# 总结

通过这一次的一个体验过程，我总结了一下几个优势：

Cloud Studio 作为 Web IDE/在线 IDE/Cloud IDE，和本地 IDE 相比具有以下优势：

-**无需安装，跨平台**：只要有浏览器就可以使用；预置常用环境，无需手动安装；支持创建网页预览，在线开发调试。


-**全功能**：无需下载安装，随时随地开发编码，拥有媲美本地 IDE 的流畅编码体验。


-**多环境**：内置 Node.js、Java、Python 等常见环境，也可以连接到云服务器进行资源管理。


-**兼容 VS Code 插件**：若默认的配置无法满足需求，可以在线安装 VS Code 插件来增强使用体验。


-**持久化和快速加载**：随开随写，随时保存，再也无需担心断电未保存，不浪费您的每一份灵感。

在我的体验下，概括来说就是Cloud Studio 是用来开发中小型项目，在线修改代码，或者连接云服务器进行部署工作的不二之选。真正的达到了一键秒开、全持久化、预置环境及内置开发工具，跨团队无缝复制和共享，让开发化繁为简。














