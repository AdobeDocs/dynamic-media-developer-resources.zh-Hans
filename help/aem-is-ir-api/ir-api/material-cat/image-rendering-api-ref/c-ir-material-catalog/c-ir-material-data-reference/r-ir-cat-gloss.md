---
description: 表面光泽度指定材料表面的相对光泽度。
solution: Experience Manager
title: 光泽
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 3%

---


# 光泽{#gloss}

表面光泽度指定材料表面的相对光泽度。

此值由呈示器用于以下目的：

* 当`catalog::Illum`为–1时，选择照明映射。
* 结合`catalog::Type`控制光泽效果（镜面反射）渲染。
* 与`catalog::Type`和`catalog::Roughness`一起控制3D反射渲染效果。

## 属性 {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

整数。 范围0...100中的百分比数。 所有材料均为可选。 仅用于具有多个反射图的晕影或具有3D反射功能的晕影。 留空或设置为–1（如果不知道或不需要）。

## 默认 {#section-2352721073524f1a8d461f64a363aac9}

如果此值设置为–1，则晕影将提供默认值。

## 另请参阅 {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , catalog: [:Ruensity](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [ catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
