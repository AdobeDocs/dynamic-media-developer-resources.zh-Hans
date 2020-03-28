---
description: 有关安装Scene7查看器API的说明。
seo-description: 有关安装Scene7查看器API的说明。
seo-title: 在同一服务器上安装多个查看器
solution: Experience Manager
title: 在同一服务器上安装多个查看器
topic: Dynamic media
uuid: 91ae8eb5-1d23-4fa3-a0d6-a4a0ed0eb104
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 在同一服务器上安装多个查看器{#installing-multiple-viewers-on-the-same-server}

有关安装Scene7查看器API的说明。

安装图像服务查看器之前，请先安装并测试图像服务。

将IS查看器文件复制到您的硬盘驱动器，然后将该 `s7viewers.war` 文件部署到目 `../ImageServing/webapps` 录中。 有关如何部署、开始、停止和管理图像服务器的说明，请参阅图像服务文档。

>[!NOTE]
>
>没有为图像服务查看器安装升级。 Adobe建议您先备份任何现有的Scene7查看器目录，然后再继续安装。

**在同一服务器上安装查看器**

1. 将查看器。war重命名为所需的上下文，并将文件部署到所需位置。
1. 在中 `this.isViewerRoot` 设置参数 `config.js`。
1. 打开 `config.js` 位于新创建的查看器文件夹根目录下的文件夹。
1. 将参数 `this.isViewerRoot = "/s7viewers"` 设置为文件的上 `s7viewers.war` 下文。 示例, `"/s7viewers-4.0"`. 保存并关闭文件。
1. 保存文件并关闭。
