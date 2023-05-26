---
title: 在同一台服务器上安装多个Dynamic Media查看器
description: Dynamic Media查看器API的安装说明。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 7a8d7205-d3bf-4ca8-b80a-9072436a3df5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# 在同一服务器上安装多个查看器{#installing-multiple-viewers-on-the-same-server}

<!-- Updated April 06, 2021 from https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=scene7qa&title=s7Viewers%2C+S7SDK%2C+S7OnDemand+Release+Notes - Contact is Sasha -->

Dynamic Media查看器API的安装说明。

在安装图像服务查看器之前，请安装和测试图像服务。

将IS查看器文件复制到硬盘驱动器，然后部署 `s7viewers.war` 文件放入中 `../ImageServing/webapps` 目录。 有关如何部署、启动、停止和管理图像服务器的说明，请参阅图像服务文档。

>[!NOTE]
>
>没有为图像服务查看器安装升级。 Adobe建议，在继续安装之前，备份任何现有的Dynamic Media查看器(s7viewers)目录。

**要在同一服务器上安装多个查看器，请执行以下操作：**

1. 将查看器.war重命名为所需的上下文，并将文件部署到所需的位置。
1. 设置 `this.isViewerRoot` 中的参数 `config.js`.
1. 打开 `config.js` 位于新创建的查看器文件夹的根目录下。
1. 设置参数 `this.isViewerRoot = "/s7viewers"` 到的上下文 `s7viewers.war` 文件。 例如，`"/s7viewers-4.0"`。
1. 保存文件并关闭。
