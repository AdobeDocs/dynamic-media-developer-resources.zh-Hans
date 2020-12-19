---
description: 缩略图图像。 请求使用目录缩略图条件格式化和调整大小的图像数据。
seo-description: 缩略图图像。 请求使用目录缩略图条件格式化和调整大小的图像数据。
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 0%

---


# tmb{#tmb}

缩略图图像。 请求使用目录缩略图条件格式化和调整大小的图像数据。

`req=tmb`

回复数据格式和响应MIME类型由`fmt=`确定。 支持除`fit=`之外的所有命令。

请参阅[缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)。

HTTP响应可以基于`catalog::Expiration`以TTL缓存。
