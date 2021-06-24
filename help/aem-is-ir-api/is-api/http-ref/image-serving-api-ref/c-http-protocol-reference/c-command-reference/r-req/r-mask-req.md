---
description: 图像蒙版。 请求掩码（Alpha通道）数据。
solution: Experience Manager
title: 蒙版
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 12%

---

# 蒙版{#mask}

图像蒙版。 请求掩码（Alpha通道）数据。

`req=mask`

支持与`req=img`相同的命令。 服务器会以相同方式处理该数据，但服务器不会返回RGB或RGBA数据，而是会丢弃颜色信息，仅返回掩码（Alpha通道）数据。 回复数据格式和响应MIME类型由`fmt=`确定。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.
