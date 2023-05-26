---
title: 解析模式
description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样和插值属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# 解析模式{#resmode}

默认重新取样模式。 指定用于缩放图像数据的默认重新取样和插值属性。

使用时间 `resMode=` 未在请求中指定。

## 属性 {#section-493f900be522486f97710cebdc4460c2}

枚举。 设置为2，表示 `bilin`， 3表示 `bicub`，或4表示 `sharp2` 插值模式(请参见 [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) 了解详细信息)。 `sharp` (1)已被弃用。 使用 `sharp2` (4)取而代之，以获得最佳结果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

继承自 `default::ResMode` 如果未定义或为空。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
