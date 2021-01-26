---
description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
seo-description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
seo-title: 服务器管理概述
solution: Experience Manager
title: 服务器管理概述
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 0%

---


# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Dynamic Media图像渲染服务器。

图像渲染由两个主要组件组成：

* Java包与Image Serving Platform Server一起部署，并管理客户端连接、缓存和材料目录。
* 本机代码模块部署为图像服务器的扩展库并实现核心图像渲染功能。

这两个组件统称为&#x200B;*Render Server*。

图像渲染与图像服务共享许多服务器设施，所有选项都通过编辑配置文件进行配置。 其他配置属性由默认目录([!DNL default.ini])或特定材料目录提供。 有关详细信息，请参阅材料目录。

图像渲染安装文件夹(*[!DNL install_folder]*)为[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认&#x200B;*[!DNL install_root]*&#x200B;为`C:\Program Files\Scene7`。 安装过程中可以指定其他文件夹。 在Linux上，*[!DNL install_root]*&#x200B;必须始终为[!DNL /usr/local/scene7]。 可以使用符号链接。

所有文件路径在UNIX上区分大小写，在Windows上不区分大小写。
