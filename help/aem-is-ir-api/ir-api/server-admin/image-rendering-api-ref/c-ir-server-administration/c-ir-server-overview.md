---
description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
solution: Experience Manager
title: 服务器管理概述
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Dynamic Media图像渲染服务器。

图像渲染由两个主要组件组成：

* Java包随Image Serving Platform Server一起部署，并管理客户端连接、缓存和材料目录。
* 本机代码模块被部署为图像服务器的扩展库并实现核心图像呈现功能。

这两个组件统称为&#x200B;*Render Server*。

“图像渲染”与“图像服务”共享许多服务器功能，所有选项都可通过编辑配置文件进行配置。 其他配置属性由默认目录([!DNL default.ini])或特定材料目录提供。 有关详细信息，请参阅材料目录。

映像渲染安装文件夹(*[!DNL install_folder]*)为[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认&#x200B;*[!DNL install_root]*&#x200B;为`C:\Program Files\Scene7`。 安装过程中可以指定其他文件夹。 在Linux上，*[!DNL install_root]*&#x200B;必须始终为[!DNL /usr/local/scene7]。 可以使用符号链接。

所有文件路径在UNIX上均区分大小写，在Windows上均不区分大小写。
