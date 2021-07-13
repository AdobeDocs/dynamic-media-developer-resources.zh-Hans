---
description: 缩略图。 请求使用目录缩略图条件设置格式并调整大小的图像数据。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

缩略图。 请求使用目录缩略图条件设置格式并调整大小的图像数据。

`req=tmb`

回复数据格式和响应MIME类型由`fmt=`确定。 支持除`fit=`以外的所有命令。

请参阅[缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)。

HTTP响应可以基于`catalog::Expiration`缓存TTL。
