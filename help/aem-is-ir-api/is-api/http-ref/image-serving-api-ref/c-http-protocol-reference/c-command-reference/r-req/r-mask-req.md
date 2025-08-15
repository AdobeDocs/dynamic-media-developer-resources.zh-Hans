---
description: 图像蒙版。 请求掩码（Alpha通道）数据。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# 蒙版{#mask}

图像蒙版。 请求掩码（Alpha通道）数据。

`req=mask`

支持与`req=img`相同的命令。 服务器以相同的方式处理，但服务器不会返回RGB或RGBA数据，而是丢弃颜色信息并仅返回蒙版（alpha通道）数据。 回复数据格式和响应MIME类型由`fmt=`确定。

可使用基于`catalog::Expiration`的TTL来缓存HTTP响应。
