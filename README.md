---
title: '【腾讯云Cloud Studio实战训练营】使用Cloud Studio&Flutter完成跨平台博客的搭建'
subTitle: '使用Cloud Studio&Flutter完成跨平台博客的搭建'
summary: '本文我将使用Cloud Studio 以及Flutter完成自己的一个博客平台的搭建。并且会将该项目作为模版，供大家使用。'
tags: ['用户体验']
date: '2023-07-22'
author: '徐建国'
avatar: 'https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-0.png'
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

Cloud Studio 作为在线IDE，包含代码高亮、自动补全、Git集成、终端等IDE的基础功能，同时支持实时调试、插件扩展等，可以帮助开发者快速完成各种应用的开发、编译与部署工作。我将这次的这个博客网站使用Cloud Studio推送到了Gitee，[大家可以访问]([https://cloudstudio.net](https://gitee.com/jianguo888/flutter_bloc_super))
[CODING](https://coding.net/)
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

**2.2实时调试网页**

Cloud Studio 支持您连接自己的云服务器，这样就可以在编辑器中查看云服务器上的文件，进行在线编程和部署工作。

只有有自己的云服务器，那么你就可以在这里通过配置，很方便的入手开发。

![](https://help-assets-1257242599.cos.ap-shanghai.myqcloud.com/enterprise/2023/1/1-10.png)


# 三.登录注册

Cloud Studio 在线编程平台支持使用[CODING (opens new window)]([https://coding.net/?from_column=20420&from=20420))账号和 GitHub 账号，以及微信登录，可以在[登录 (opens new window)]([https://cloudstudio.net/auth/realms/cloudstudio/protocol/openid-connect/auth?client_id=cloudstudio-apiserver&response_type=code&redirect_uri=https%3A%2F%2Foauth.cloudstudio.net%2Fapi%2Fpublic%2Foauth%2Fcallback%3Fsrc%3D%252F&team=&kc_idp_hint=))
界面输入相应的账号登录前往 Web IDE，这里我用的是微信登录。









![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/01.png)

你可以播放下方视频了解本次实战的全流程。文字版内容可参考剩余章节。

<video
  webkit-playsinline='true'
  playsInline={true}
  controls
  controlsList='nodownload'
  preload='auto'
  src='https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/video.mp4'
></video>

# 项目准备

我们以 Flutter 团队提供的一个[教程项目](https://codelabs.developers.google.com/codelabs/flutter-boring-to-beautiful?hl=zh-cn#0)为例子，演示仅通过**浏览器**实现一个 Flutter 项目开发的全过程。

## 创建项目

首先，在 [CODING](https://coding.net) 中新建一个项目，命名并填写项目相关信息。如没有 [CODING](https://coding.net) 团队，需要先进行免费注册。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/02.png)

## 代码拉取

创建完项目之后，即可在左边栏中进入**代码仓库**创建仓库拉取项目代码，这里我们选择「**点击导入**」。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/03.png)

填写仓库地址并进行命名，点击「**完成创建**」，等待仓库导入成功后，即可看到项目代码。至此，项目准备完成。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/04.png)

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/05.png)

# 在线编码

在上一步中，我们完成了项目准备，现在，我们可以在 [Cloud Studio](https://cloudstudio.net/) 中导入这个项目，进行代码**编写**、**调试**和**预览**。

## 创建工作空间

由于 [CODING](https://coding.net/) 和 [Cloud Studio](https://cloudstudio.net/) 实现了账号互通，我们可以用 **CODING 账号**登录，完成账号授权。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/06.png)

登录完成后，在左下角点击创建**工作空间**，导入 [CODING](https://coding.net/) 内的代码仓库，并且选择预设好 Flutter 环境的**开发环境**，点击创建，等待几秒，一个崭新的工作空间即创建完成。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/07.png)

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/08.png)

## 安装插件与依赖

[Cloud Studio](https://cloudstudio.net/) 与 VS code 一样，集成了许多**开发插件**。

我们可以通过在线安装 VSCode 插件增强使用体验。

1. 在左边栏选择「**扩展**」，安装 Flutter 和 Dart 插件，下载完成中点击**重新加载**即可完成插件安装。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/09.png)

2. 打开终端，我们还需要初始化项目的依赖：

```shell
# 加载项目依赖

flutter pub get
```

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/10.png)

3. 提示 Dart 版本太低，我们需要先更新 Flutter：

```shell
# 更新 Flutter 版本，先后执行以下命令

flutter channel stable

flutter upgrade
```

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/11.png)

4. 再次执行 `flutter pub get` 完成依赖加载。

## 项目启动/调试

执行完上一步的前置步骤后，现在，我们可以**启动项目**。

[Cloud Studio](https://cloudstudio.net/) 可以快速生成**预览链接**，方便分享他人**展示项目**或**在线调试**。

1. 首先执行 run 命令，将项目以 web 方式启动到 9000 端口。

```shell
# 启动

flutter run -d web-server --web-port 9000 --web-hostname 0.0.0.0
```

2. 点击内置浏览器，即可看到预览效果 ，我们可以将这个链接分享给他人，他们可以**远程**打开该链接。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/12.png)

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/13.png)

接下来，我们将演示如何修改代码，并通过项目热加载快速看到修改结果。我们将会添加左边导航栏的图标，以便用户快速浏览前置图标以找到所需标签页。

1. 找到 lib/src/shared/router.dart

2. 替换 icon 代码，为每个导航目的地（首页、播放列表和用户）添加不同的前置图标：

```dart
const List<NavigationDestination> destinations = [
  NavigationDestination(
    label: 'Home',
    icon: Icon(Icons.home), // Modify this line
    route: '/',
  ),
  NavigationDestination(
    label: 'Playlists',
    icon: Icon(Icons.playlist_add_check), // Modify this line
    route: '/playlists',
  ),
  NavigationDestination(
    label: 'Artists',
    icon: Icon(Icons.people), // Modify this line
    route: '/artists',
  ),
];
```

3. 修改完成后，在终端中输入 q 进行**热加载**。

4. 等待片刻，刷新页面即可看到最新的效果。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/14.png)

## 提交代码

[Cloud Studio](https://cloudstudio.net/) 也提供了图形化的源代码管理界面，左侧点击**源代码管理**，**暂存**我们刚刚修改了的文件，填写 **commit message**，点击「**提交**」和「**同步更改**」，即可提交代码到 [CODING](https://coding.net/)。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/15.png)

至此，我们已经在 [Cloud Studio](https://cloudstudio.net/) 完成了**编写**、**调试**和**预览**。

通过重复迭代，我们开发了一个满意的代码版本。

接下来，我会演示如何通过 [CODING](https://coding.net/) **持续集成流水线**实现**自动化打包**。

# CODING 打包 apk 制品

首先，介绍一下什么是持续集成。以下是来自 [CODING 帮助文档](https://coding.net/help/docs/ci/intro.html)的介绍。

![](https://help-assets.codehub.cn/enterprise/20230331160037.png)

像**代码打包**这种重复性的工作，我们可以交给**持续集成**来完成，以下是使用步骤。

1. 首先我们在项目的**制品管理**中新建一个制品，用于存放生存的 apk 文件。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/16.png)

2. 然后在左侧导航栏点击**持续集成**，新建一个构建计划。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/17.png)

3. 在自定义构建过程中选择我们刚刚创建的仓库，点击确认进入**流水线**编辑。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/21.png)

本次 Flutter 的打包分为 4 个部分：

- jdk 升级（由于 CODING 构建机默认是 jdk 1.8，我们需要升级成 jdk11）
- 代码检出

- 打包 apk

- 推送带制品仓库

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/18.png)

```shell
pipeline {
  agent any
  stages {
    stage('jdk upgrade') {
      steps {
        sh 'sudo add-apt-repository ppa:openjdk-r/ppa'
        sh 'sudo apt-get update'
        sh 'sudo apt-get install -y openjdk-11-jdk'
        sh 'java -version'
      }
    }

    stage('检出') {
      steps {
        checkout([
          $class: 'GitSCM',
          branches: [[name: GIT_BUILD_REF]],
          userRemoteConfigs: [[
            url: GIT_REPO_URL,
            credentialsId: CREDENTIALS_ID
          ]]])
        }
      }

      stage('打包 apk') {
        steps {
          sh 'sudo apt-get install --only-upgrade bash'
          sh 'wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.7.6-stable.tar.xz'
          sh 'tar xf flutter_linux_3.7.6-stable.tar.xz'
          sh 'export PATH="$PATH:`pwd`/flutter/bin" && cd ${PROJECT_PATH} && flutter build apk'
        }
      }

      stage('推送到制品仓库') {
        steps {
          codingArtifactsGeneric(files: '${PROJECT_PATH}/build/app/outputs/flutter-apk/**.apk', repoName: 'apk')
        }
      }

    }
    environment {
      JAVA_HOME = '/usr/lib/jvm/java-11-openjdk-amd64'
    }
  }
```

4. 完成流水线后，点击「**立即构建**」。

如下图，流水线已经构建成功，进入制品仓库中可以看到构建后的 apk 制品。

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/19.png)

![](https://help-assets.codehub.cn/enterprise/new-static/images/insight/flutter/20.png)

# 总结

至此，我们通过 [Cloud Studio](https://cloudstudio.net) 和 [CODING](https://coding.net) 配合使用，只使用浏览器便实现了 Flutter 项目在云端的**创建、开发、管理、打包**的全过程。

另外, [Cloud Studio](https://cloudstudio.net) 提供了许多编程语言的**模板和开发环境**，也集成了腾讯云 Serverless 技术，把前端开发项目、静态建站项目的**部署复杂度降到最低**，一键即可完成**线上部署**。

不仅如此， [Cloud Studio](https://cloudstudio.net) 中还有一个 [metawork](https://cloudstudio.net/metawork) 协同套件，可以支持多人线上**协同编码**，可以跟同学、同事共同线上开发，实现 coding anytime anyway！
