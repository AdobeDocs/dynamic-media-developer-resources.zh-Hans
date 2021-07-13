---
description: 图像（默认）。 请求标准图像数据。
solution: Experience Manager
title: img
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 5338358e-755b-41d6-a941-8754d0deb9aa
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 20%

---

# img{#img}

图像（默认）。 请求标准图像数据。

`req=img`

回复数据格式和响应MIME类型由`fmt=`确定。 `req=img` 是默认的请求类型，无需明确指定。HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他请求命令将按说明进行应用。
