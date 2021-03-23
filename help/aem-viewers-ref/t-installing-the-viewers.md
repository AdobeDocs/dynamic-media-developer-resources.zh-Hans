---
title: 在同一服务器上安装多个Dynamic Media查看器
description: 有关安装Dynamic Media Viewer API的说明。
solution: Experience Manager
feature: Dynamic Media Classic，查看器，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# 在同一服务器上安装多个查看器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated January 13, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

有关安装Dynamic Media查看器API的说明。

安装图像服务查看器之前，请先安装并测试图像服务。

将IS查看器文件复制到硬盘，然后将`s7viewers.war`文件部署到`../ImageServing/webapps`目录中。 有关如何部署、开始、停止和管理图像服务器的说明，请参阅图像服务文档。

>[!NOTE]
>
>没有为图像服务查看器安装升级。 Adobe建议您在继续安装之前备份任何现有的Dynamic Media查看器(s7viewers)目录。

**在同一服务器上安装多个查看器**

1. 将查看器.war重命名为所需的上下文，并将文件部署到所需位置。
1. 在`config.js`中设置`this.isViewerRoot`参数。
1. 打开位于新创建的查看器文件夹根目录中的`config.js`。
1. 将参数`this.isViewerRoot = "/s7viewers"`设置为`s7viewers.war`文件的上下文。 例如，`"/s7viewers-4.0"`。
1. 保存文件并关闭。
