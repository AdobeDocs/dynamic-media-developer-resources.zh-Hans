---
description: 地址筛选器元素。 在<rule>元素中为可选。 在应用规则时覆盖属性ClientAddressFilter。
seo-description: 地址筛选器元素。 在<rule>元素中为可选。 在应用规则时覆盖属性ClientAddressFilter。
seo-title: 地址筛选器
solution: Experience Manager
title: 地址筛选器
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 4%

---


# 地址筛选器{#addressfilter}

地址筛选器元素。 在`<rule>`元素中为可选。 覆盖属性：：应用规则时的ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

以逗号分隔的IP地址列表。 每个单独的地址可以包括可选的网络掩码后缀以允许IP地址范围的规范。 有关详细信息，请参阅` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通过在`<addressfilter>`元素中指定此图像目录，可限制对一个或多个特定IP地址的访问。 如果客户端IP地址不匹配，则向客户端返回“请求拒绝”错误。

如果`<addressfilter>`为空或未指定，则访问不受限制。

如果`<rule>`元素中的`<expression>`不存在或为空，则`<addressfilter>`将应用于所有请求。

`localhost` 始终是定义的隐 `ClientAddressFilter` 式部分，即使未显式指定。始自`localhost`的请求从不被拒绝，无论`ClientAddressFilter`规范如何。

## SeeaAllo {#section-02056065e0c042e1b155b2f3e5b84ef7}

[属性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
