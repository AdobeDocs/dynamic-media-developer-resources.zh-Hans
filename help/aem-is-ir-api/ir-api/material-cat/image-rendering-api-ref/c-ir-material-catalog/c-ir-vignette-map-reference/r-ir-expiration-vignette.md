---
description: 客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 6%

---

# 過期{#expiration}

客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。

有关详细信息，请参阅` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`。

## 属性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

实数、-2、-1、0或更大。 自生成响应图像后到期的小时数。 设置为0始终使响应图像立即过期，这会有效地禁用客户端缓存。 设置为–1以标记为`never expire`;在这种情况下，服务器始终返回403状态以响应条件`GET`请求，而不检查文件是否已实际更改。 设置为–2时，将使用`attribute::Expiration`提供的默认值。

## 默认 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果字段不存在，则当值为–2或字段为空时，将使用。

## 另请参阅 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[属性：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
