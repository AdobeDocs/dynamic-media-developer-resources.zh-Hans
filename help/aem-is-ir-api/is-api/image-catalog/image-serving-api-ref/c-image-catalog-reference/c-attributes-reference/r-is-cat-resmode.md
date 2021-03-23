---
description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。
seo-description: 默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。
seo-title: ResMode
solution: Experience Manager
title: ResMode
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# ResMode{#resmode}

默认重新取样模式。 指定用于缩放图像数据的默认重新取样属性和插值属性。

在请求中未指定`resMode=`时使用。

## 属性 {#section-493f900be522486f97710cebdc4460c2}

枚举。 对于`bilin`，设置为2；对于`bicub`，设置为3；对于`sharp2`插值模式，设置为4（有关详细信息，请参阅` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)`）。 `sharp` (1)已弃用。请改用`sharp2`(4)以获得最佳效果。

## 默认 {#section-35f980e745fc4d79a2621e8abacc724d}

如果未定义或为空，则从`default::ResMode`继承。

## 另请参阅 {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
