---
description: 客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。
solution: Experience Manager
title: 過期
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# 過期{#expiration}

客户端缓存生存时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。

参见 [catalog：：到期](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md) 了解详细信息。

## 属性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

实数、-2、-1、0或更大。 自生成响应图像以来到到期为止的小时数。 设置为0可始终使响应图像立即过期，这可以有效地禁用客户端缓存。 设置为–1以标记为 `never expire`；在这种情况下，服务器始终返回403状态以响应条件响应 `GET` 请求而不检查文件是否实际发生了更改。 设置为–2以使用提供的默认值 `attribute::Expiration`.

## 默认 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果字段不存在、值为–2或字段为空，则使用。

## 另请参阅 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[attribute：：Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ， [catalog：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)， [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
