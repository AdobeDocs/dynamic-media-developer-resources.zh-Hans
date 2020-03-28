---
description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
seo-description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
seo-title: 地址过滤器
solution: Experience Manager
title: 地址过滤器
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 地址过滤器{#addressfilter}

地址筛选器元素。 在和元 `<rule>` 素中 `<pathrule>` 可选。

应用 `attribute::ClientAddressFilter` 规则时覆盖。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

无。

## 数据 {#section-c762bdfe425140d689ea5abf25e9a48a}

以逗号分隔的IP地址列表。 每个单独的地址可以包括可选的网络掩码后缀以允许IP地址范围的规范。 有关详细信息，请参阅`attribute::ClientAddressFilter`。

## 说明 {#section-d561b2485e004ef8a2085997d0f4bca6}

通过在元素中指定此图像目录的访问权限，可以限制为一个或多个特定客户端IP `<addressfilter>` 地址。 如果客户端IP地址不匹配，则向客户端返回“请求已拒绝”错误。

如果为空或未指定， `<addressfilter>` 则访问不受限制。

如果元 `<expression>` 素中的 `<rule>` 元素缺失或为空，则该元素将应 `<addressfilter>` 用于所有请求。

## 另请参阅 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[属性：:ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
