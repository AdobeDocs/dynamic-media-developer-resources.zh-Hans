---
description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
seo-description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
seo-title: 地址筛选器
solution: Experience Manager
title: 地址筛选器
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 6%

---


# 地址筛选器{#addressfilter}

地址筛选器元素。 在`<rule>`和`<pathrule>`元素中是可选的。

应用规则时覆盖`attribute::ClientAddressFilter`。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

无。

## 数据 {#section-c762bdfe425140d689ea5abf25e9a48a}

以逗号分隔的IP地址列表。 每个单独的地址可以包括可选的网络掩码后缀以允许IP地址范围的规范。 有关详细信息，请参阅`attribute::ClientAddressFilter`。

## 说明 {#section-d561b2485e004ef8a2085997d0f4bca6}

通过在`<addressfilter>`元素中指定此映像目录，可以限制对一个或多个特定客户端IP地址的访问。 如果客户端IP地址不匹配，则向客户端返回“请求拒绝”错误。

如果`<addressfilter>`为空或未指定，则访问不受限制。

如果`<rule>`元素中的`<expression>`不存在或为空，则`<addressfilter>`将应用于所有请求。

## 另请参阅 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[属性：:ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
