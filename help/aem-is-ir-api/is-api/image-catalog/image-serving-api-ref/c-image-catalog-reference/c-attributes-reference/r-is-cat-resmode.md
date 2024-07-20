---
title: 解析模式
description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样和插值属性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 3%

---

# 解析模式{#resmode}

默认重新取样模式。 指定用于缩放图像数据的默认重新取样和插值属性。

在请求中未指定`resMode=`时使用。

## 属性 {#section-493f900be522486f97710cebdc4460c2}

枚举。 对于`bilin`，设置为2；对于`bicub`，设置为3；对于`sharp2`插值模式，设置为4（有关详细信息，请参阅[resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md)）。 `sharp` (1)已被弃用。 请改用`sharp2` (4)以获得最佳结果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

如果未定义或为空，则从`default::ResMode`继承。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
