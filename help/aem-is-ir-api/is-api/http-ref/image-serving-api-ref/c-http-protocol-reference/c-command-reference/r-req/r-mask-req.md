---
description: 图像蒙版。 请求掩码(alpha渠道)数据。
seo-description: 图像蒙版。 请求掩码(alpha渠道)数据。
seo-title: 遮罩
solution: Experience Manager
title: 遮罩
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 11%

---


# mask{#mask}

图像蒙版。 请求掩码(alpha渠道)数据。

`req=mask`

服务器支持与`req=img`相同的命令，并且服务器以相同的方式处理这些命令，但服务器不返回RGB或RGBA数据，而是丢弃颜色信息并只返回掩码(alpha渠道)数据。 回复数据格式和响应MIME类型由`fmt=`确定。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
