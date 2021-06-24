---
description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。

在请求中未指定`resMode=`时使用。

## 属性 {#section-493f900be522486f97710cebdc4460c2}

枚举。 对于`bilin`，设置为2；对于`bicub`，设置为3；对于`sharp2`插值模式，设置为4（有关详细信息，请参阅` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`）。 `sharp` (1)正在被弃用。请改用`sharp2`(4)以获得最佳结果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

从`default::ResMode`继承（如果未定义或为空）。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
