---
description: 地址筛选器元素。 在<rule>元素中为可选。 在应用规则时覆盖属性ClientAddressFilter。
seo-description: 地址筛选器元素。 在<rule>元素中为可选。 在应用规则时覆盖属性ClientAddressFilter。
seo-title: 地址过滤器
solution: Experience Manager
title: 地址过滤器
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 地址过滤器{#addressfilter}

地址筛选器元素。 元素中为可 `<rule>` 选。 覆盖属性：：应用规则时的ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

以逗号分隔的IP地址列表。 每个单独的地址可以包括可选的网络掩码后缀以允许IP地址范围的规范。 有关详细信息，请参阅` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)`。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通过在元素中指定此图像目录，可以将访问权限限制为一个或多个特定IP `<addressfilter>` 地址。 如果客户端IP地址不匹配，则向客户端返回“请求已拒绝”错误。

如果为空或未指定， `<addressfilter>` 则访问不受限制。

如果元 `<expression>` 素中的 `<rule>` 元素缺失或为空，则该元素将应 `<addressfilter>` 用于所有请求。

`localhost` 始终隐式地包含在定 `ClientAddressFilter` 义中，即使未显式指定也是如此。 始发自的请 `localhost` 求不会被拒绝，而不管规范如 `ClientAddressFilter` 何。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[属性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
