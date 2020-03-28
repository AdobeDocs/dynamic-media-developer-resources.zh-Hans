---
description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。
seo-description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。

在请求 `resMode=` 中未指定时使用。

## 属性 {#section-493f900be522486f97710cebdc4460c2}

枚举。 对于插值模式， `bilin`设置为2表示 `bicub`，设置为3表示，或设置为4 `sharp2` 表示(有关详细信息， ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` 请参阅)。 `sharp` (1)已弃用。 请改 `sharp2` 用(4)来获得最佳效果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

如果未定义 `default::ResMode` 或为空，则从中继承。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
