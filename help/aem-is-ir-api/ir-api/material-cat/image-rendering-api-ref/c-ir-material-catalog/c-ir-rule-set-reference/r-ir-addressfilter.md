---
description: 地址筛选器元素。 可选，位于 <rule> 元素。 应用规则时覆盖属性ClientAddressFilter。
solution: Experience Manager
title: 地址过滤器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# 地址过滤器{#addressfilter}

地址筛选器元素。 可选，位于 `<rule>` 元素。 应用规则时覆盖attribute：：ClientAddressFilter。

## 属性 {#section-e7a0960f7f0045da91de37824aa4aeaa}

无。

## 数据 {#section-eb138f192516418a9ef2ab9a38c9ee9e}

IP地址的逗号分隔列表。 每个单独的地址可以包括一个可选的网络掩码后缀，以允许指定IP地址范围。 参见 [attribute：：ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) 了解详细信息。

## 说明 {#section-099b7839c4be40c68cbff29dad14e7d5}

可以通过在中指定一个或多个特定IP地址来限制对此图像目录的访问 `<addressfilter>` 元素。 如果客户端IP地址不匹配，则向客户端返回“请求被拒绝”错误。

访问不受限制，如果 `<addressfilter>` 为空或未指定。

如果 `<expression>` 在 `<rule>` 元素不存在或为空， `<addressfilter>` 应用于所有请求。

`localhost` 始终隐式是 `ClientAddressFilter` 定义（即使未明确指定）。 请求源自 `localhost` 不会被拒绝，无论 `ClientAddressFilter` 规范。

## 另请参阅 {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute：：ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
