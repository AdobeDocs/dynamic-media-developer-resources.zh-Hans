---
description: 客户端缓存的实时时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。
seo-description: 客户端缓存的实时时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。
seo-title: 過期
solution: Experience Manager
title: 過期
topic: Scene7 Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 过期时间{#expiration}

客户端缓存的实时时间。 到期前的小时数。 用于管理客户端和代理服务器缓存。

有关详细信息，请参阅` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)`。

## 属性 {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

实数、-2、-1、0或更大。 自生成响应图像以来到期的小时数。 设置为0可始终立即使响应映像过期，这会有效地禁用客户端缓存。 设置为-1以标记为 `never expire`;在这种情况下，服务器始终会返回403状态以响应条件请 `GET` 求，而不检查文件是否实际更改。 设置为-2以使用由提供的默认值 `attribute::Expiration`。

## 默认 {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` 如果字段不存在、值为-2或字段为空，则使用。

## 另请参阅 {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[属性：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ，目 [录：:Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
