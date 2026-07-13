---
description: 本文档介绍如何管理Dynamic Media图像渲染服务器。
solution: Experience Manager
title: 服务器管理概述
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 294cd068-8676-4932-a3ad-1a3c5bfa691e
TQID: 'https://experienceleague.adobe.com/t9zGehwMxhHq1HrP3mmNGvkthmqYxX2ijeyihn5OEWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 163
ht-degree: 0%

---

# 服务器管理概述{#server-administration-overview}

本文档介绍如何管理Dynamic Media图像渲染服务器。

图像渲染包含两个主要组件：

* Java包随图像服务[!DNL Platform Server]一起部署，用于管理客户端连接、缓存和材料目录。
* 本机代码模块部署为图像服务器的扩展库，并实施核心图像渲染功能。

这两个组件统称为&#x200B;*渲染服务器*。

图像渲染与图像服务共享许多服务器功能，所有选项都通过编辑配置文件进行配置。 默认目录([!DNL default.ini])或特定材质目录提供了其他配置属性。 有关详细信息，请参阅物料目录。

图像渲染安装文件夹(*[!DNL install_folder]*)是[!DNL *[!DNL install_root]*/ImageRendering]。 在Windows上，默认&#x200B;*[!DNL install_root]*&#x200B;为`C:\Program Files\Scene7`。 安装过程中可以指定其他文件夹。 在Linux上，*[!DNL install_root]*&#x200B;必须始终为[!DNL /usr/local/scene7]。 可以使用符号链接。

所有文件路径在UNIX上均区分大小写，在Windows上则不区分大小写。

