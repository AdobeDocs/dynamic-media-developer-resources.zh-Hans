---
description: 图像蒙版。 请求掩码(Alpha渠道)数据。
seo-description: 图像蒙版。 请求掩码(Alpha渠道)数据。
seo-title: 蒙版
solution: Experience Manager
title: 蒙版
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 10%

---


# mask{#mask}

图像蒙版。 请求掩码(Alpha渠道)数据。

`req=mask`

服务器支持与`req=img`相同的命令，并且服务器以相同的方式处理这些命令，但服务器不返回RGB或RGBA数据，而是丢弃颜色信息并仅返回蒙版(alpha渠道)数据。 回复数据格式和响应MIME类型由`fmt=`确定。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
