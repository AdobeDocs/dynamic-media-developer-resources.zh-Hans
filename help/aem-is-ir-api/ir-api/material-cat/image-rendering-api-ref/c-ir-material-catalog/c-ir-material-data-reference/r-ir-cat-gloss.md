---
description: 表面光泽度指定材料表面的相对光泽度。
solution: Experience Manager
title: 光泽
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# 光泽{#gloss}

表面光泽度指定材料表面的相对光泽度。

呈现器将使用此值用于以下目的：

* 当`catalog::Illum`为–1时，选择照明图。
* 控制与`catalog::Type`一起呈现的光泽效果（镜面反射）。
* 控制3D反射渲染效果与`catalog::Type`和`catalog::Roughness`结合使用。

## 属性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 范围0...100中的百分比数字。 适用于所有材料的可选。 仅用于具有多个反射图的晕影或具有3D反射功能的晕影。 将留空，或将其设置为–1（如果不知道或不需要）。

## 默认 {#section-2352721073524f1a8d461f64a363aac9}

如果将此值设置为–1，则晕影会提供默认值。

## 另请参阅 {#section-0213bbdb7d6d4974a7c53822957717c1}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ，目 [录：：粗糙度](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [目录：：类型](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
