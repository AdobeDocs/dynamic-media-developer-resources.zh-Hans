---
description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
solution: Experience Manager
title: 服务器管理概述
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Dynamic Media图像渲染服务器。

图像渲染由两个主要组件组成：

* Java包与Image Serving Platform Server一起部署，用于管理客户端连接、缓存、材料目录。
* 本机代码模块部署为图像服务器的扩展库，并实施核心图像呈现功能。

这两个组件统称为&#x200B;*Render Server*。

“图像渲染”与“图像服务”共享许多服务器功能，所有选项都通过编辑配置文件来配置。 默认目录([!DNL default.ini])或特定材料目录提供了其他配置属性。 有关详细信息，请参阅材料目录。

“Image Rendering”安装文件夹(*[!DNL install_folder]*)为[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认的&#x200B;*[!DNL install_root]*&#x200B;为`C:\Program Files\Scene7`。 在安装过程中可以指定其他文件夹。 在Linux上，*[!DNL install_root]*&#x200B;必须始终为[!DNL /usr/local/scene7]。 可以使用符号链接。

所有文件路径在UNIX上区分大小写，在Windows上不区分大小写。
