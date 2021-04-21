---
description: 图像蒙版。 请求掩码(Alpha渠道)数据。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 11%

---


# mask{#mask}

图像蒙版。 请求掩码(Alpha渠道)数据。

`req=mask`

支持与`req=img`相同的命令。 服务器以相同方式处理它，但服务器不返回RGB或RGBA数据，而是丢弃颜色信息并仅返回蒙版(alpha渠道)数据。 回复数据格式和响应MIME类型由`fmt=`确定。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
