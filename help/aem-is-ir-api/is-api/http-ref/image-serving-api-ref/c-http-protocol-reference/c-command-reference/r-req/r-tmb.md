---
description: 缩略图图像。 请求使用目录缩略图标准设置图像数据的格式和大小。
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 0%

---

# tmb{#tmb}

缩略图图像。 请求使用目录缩略图标准设置图像数据的格式和大小。

`req=tmb`

回复数据格式和响应MIME类型由 `fmt=`. 支持所有命令，但 `fit=`.

参见 [缩略图缩放](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

可以使用基于以下内容的TTL缓存HTTP响应： `catalog::Expiration`.
