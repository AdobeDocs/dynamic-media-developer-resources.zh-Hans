---
description: 缩略图。 请求使用目录缩略图条件格式化和调整大小的图像数据。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---


# tmb{#tmb}

缩略图。 请求使用目录缩略图条件格式化和调整大小的图像数据。

`req=tmb`

回复数据格式和响应MIME类型由`fmt=`确定。 支持除`fit=`外的所有命令。

请参阅[缩览图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)。

HTTP响应可以基于`catalog::Expiration`使用TTL缓存。
