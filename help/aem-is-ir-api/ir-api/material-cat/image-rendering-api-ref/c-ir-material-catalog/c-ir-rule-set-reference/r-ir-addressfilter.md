---
description: 地址筛选器元素。 在中可选 <rule> 元素。 在应用规则时覆盖属性ClientAddressFilter。
solution: Experience Manager
title: 地址筛选器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 地址筛选器{#addressfilter}

地址筛选器元素。 在中可选 `<rule>` 元素。 应用规则时覆盖属性：:ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

以逗号分隔的IP地址列表。 每个地址可以包括可选网络掩码后缀，以允许指定IP地址范围。 请参阅 [属性：:ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) 以了解详细信息。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

通过在 `<addressfilter>` 元素。 如果客户端IP地址不匹配，则会向客户端返回“请求拒绝”错误。

如果 `<addressfilter>` 为空或未指定。

如果 `<expression>` 在 `<rule>` 元素不存在或为空， `<addressfilter>` 将应用于所有请求。

`localhost` 始终隐式包含在 `ClientAddressFilter` 定义，即使未明确指定也是如此。 来自 `localhost` 不会被拒绝，无论 `ClientAddressFilter` 规范。

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[属性：:ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
