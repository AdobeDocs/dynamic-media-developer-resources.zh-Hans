---
description: 地址筛选器元素。 在<rule>和<pathrule>元素中为可选。
solution: Experience Manager
title: 地址筛选器
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---


# 地址筛选器{#addressfilter}

地址筛选器元素。 在`<rule>`和`<pathrule>`元素中为可选。

应用规则时覆盖`attribute::ClientAddressFilter`。

## 属性 {#section-31e9ad29e9934933ac154bccbc729172}

无。

## 数据 {#section-c762bdfe425140d689ea5abf25e9a48a}

以逗号分隔的IP地址列表。 每个单个地址可以包括可选的网络掩码后缀以允许IP地址范围的规范。 有关详细信息，请参阅`attribute::ClientAddressFilter`。

## 说明 {#section-d561b2485e004ef8a2085997d0f4bca6}

可通过在`<addressfilter>`元素中指定此映像目录，将其限制为一个或多个特定客户端IP地址。 如果客户端IP地址不匹配，则会向客户端返回“请求拒绝”错误。

如果`<addressfilter>`为空或未指定，则访问不受限制。

如果`<rule>`元素中的`<expression>`不存在或为空，则`<addressfilter>`将应用于所有请求。

## 另请参阅 {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
