---
description: 地址筛选器元素。 <rule>元素中的可选。 应用规则时覆盖属性ClientAddressFilter。
solution: Experience Manager
title: 地址过滤器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 150
ht-degree: 2%

---

# 地址过滤器{#addressfilter}

地址筛选器元素。 `<rule>`元素中的可选。 应用规则时覆盖attribute：：ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP地址的逗号分隔列表。 每个单独的地址可以包括一个可选的网络掩码后缀，以允许指定IP地址范围。 有关详细信息，请参阅[attribute：：ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md)。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通过在`<addressfilter>`元素中指定此图像目录，可以将访问限制为一个或多个特定的IP地址。 如果客户端IP地址不匹配，则向客户端返回“请求被拒绝”错误。

如果`<addressfilter>`为空或未指定，则访问不受限制。

如果`<rule>`元素中的`<expression>`不存在或为空，则会将`<addressfilter>`应用于所有请求。

`localhost`始终是`ClientAddressFilter`定义的隐式部分，即使未显式指定。 无论是否遵循`ClientAddressFilter`规范，源自`localhost`的请求都不会被拒绝。

## 另请参阅 {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute：：ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
