---
description: 图像（默认）。 请求标准图像数据。
solution: Experience Manager
title: img
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 19%

---


# img{#img}

图像（默认）。 请求标准图像数据。

`req=img`

回复数据格式和响应MIME类型由`fmt=`确定。 `req=img` 是默认的请求类型，无需显式指定。HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

其他请求命令将按说明应用。
