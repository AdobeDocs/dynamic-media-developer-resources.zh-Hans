---
description: 本文档介绍如何管理Scene7图像渲染服务器。
seo-description: 本文档介绍如何管理Scene7图像渲染服务器。
seo-title: 服务器管理概述
solution: Experience Manager
title: 服务器管理概述
topic: Scene7 Image Serving - Image Rendering API
uuid: 83aa83b7-bb7a-4bbd-923c-dd69763fe9c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Scene7图像渲染服务器。

图像渲染由两个主要组件组成：

* Java包随Image Serving Platform Server一起部署，并管理客户端连接、缓存和材料目录。
* 本机代码模块被部署为图像服务器的扩展库并实现核心图像渲染功能。

这两个组件统称为“渲 *染服务器”*。

图像渲染与图像服务共享许多服务器设施，所有选项都通过编辑配置文件进行配置。 其他配置属性由默认目录()或特 [!DNL default.ini]定材料目录提供。 有关详细信息，请参阅材料目录。

图像渲染安装文件夹( *[!DNL install_folder]*)为[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认 *[!DNL install_root]* 值为 [!DNL C:\Program Files\Scene7]。 安装过程中可能会指定其他文件夹。 在Linux上， *[!DNL install_root]* 必须始终为 [!DNL /usr/local/scene7]A。 可以使用符号链接。

所有文件路径在UNIX上均区分大小写，在Windows上均不区分大小写。
