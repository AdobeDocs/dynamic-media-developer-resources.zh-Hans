---
description: 表面光泽度指定材料表面的相对光泽度。
seo-description: 表面光泽度指定材料表面的相对光泽度。
seo-title: 光泽
solution: Experience Manager
title: 光泽
topic: Scene7 Image Serving - Image Rendering API
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 光泽{#gloss}

表面光泽度指定材料表面的相对光泽度。

呈示器将此值用于以下用途：

* 当为-1时，选择 `catalog::Illum` 照明映射。
* 控制光泽效果（镜面反射）渲染与之结合 `catalog::Type`。
* 结合和控制3D反射渲染效 `catalog::Type` 果 `catalog::Roughness`。

## 属性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 范围0...100中的百分比数。 对于所有材料都是可选的。 仅用于具有多个反射图的晕影或具有3D反射功能的晕影。 留空或设置为-1（如果不知道或不需要）。

## 默认 {#section-2352721073524f1a8d461f64a363aac9}

如果此值设置为-1，则暗角将提供默认值。

## 另请参阅 {#section-0213bbdb7d6d4974a7c53822957717c1}

[glouss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catalog:::Rounery](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catalog:::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
