---
description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
solution: Experience Manager
title: 服务器管理概述
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Dynamic Media图像渲染服务器。

图像渲染由两个主要组件组成：

* 将Java包与图像服务一起部署 [!DNL Platform Server] 并管理客户端连接、缓存、材料目录。
* 本机代码模块部署为图像服务器的扩展库，并实施核心图像呈现功能。

这两个组件统称为 *呈现服务器*.

“图像渲染”与“图像服务”共享许多服务器功能，所有选项都通过编辑配置文件来配置。 默认目录( [!DNL default.ini])或特定材料目录。 有关详细信息，请参阅材料目录。

映像渲染安装文件夹( *[!DNL install_folder]*)为[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认 *[!DNL install_root]* is `C:\Program Files\Scene7`. 在安装过程中可以指定其他文件夹。 在Linux上， *[!DNL install_root]* 必须始终 [!DNL /usr/local/scene7]. 可以使用符号链接。

所有文件路径在UNIX上区分大小写，在Windows上不区分大小写。
