---
title: 在同一服务器上安装多个Dynamic Media查看器
description: 有关安装Dynamic Media查看器API的说明。
solution: Experience Manager
feature: Dynamic Media Classic，查看器，SDK/API
role: Developer,Business Practitioner
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 8207cba7e75c6bff878ef7f11f74b19bb88f1d61
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 1%

---

# 在同一服务器上安装多个查看器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

有关安装Dynamic Media查看器API的说明。

在安装图像服务查看器之前，请安装并测试图像服务。

将IS查看器文件复制到硬盘，然后将`s7viewers.war`文件部署到`../ImageServing/webapps`目录。 有关如何部署、启动、停止和管理图像服务器的说明，请参阅图像提供文档。

>[!NOTE]
>
>映像服务查看器没有升级安装。 Adobe建议您在继续安装之前备份任何现有的Dynamic Media查看器(s7viewers)目录。

**要在同一服务器上安装多个查看器，请执行以下操作：**

1. 将查看器.war重命名为所需的上下文，并将文件部署到所需位置。
1. 在`config.js`中设置`this.isViewerRoot`参数。
1. 在新创建的查看器文件夹的根目录下打开`config.js`。
1. 将参数`this.isViewerRoot = "/s7viewers"`设置为`s7viewers.war`文件的上下文。 例如，`"/s7viewers-4.0"`。
1. 保存文件并关闭。
