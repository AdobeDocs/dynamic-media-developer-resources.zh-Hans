---
description: 表面粗糙度。 指定材料表面的相对光泽度。 与目录类型和目录光泽结合使用可控制3D反射渲染效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---


# 粗糙度{#roughness}

表面粗糙度。 指定材料表面的相对光泽度。 与catalog::Type and catalog::Gloss结合使用，可控制3D反射渲染效果。

## 属性 {#section-70c3f2394fd8477ca83a369448907971}

整数。 范围0...100中的百分比值。 所有材料均为可选。 仅用于具有多个反射图的晕影或具有3D反射功能的晕影。 留空或设置为–1（如果不知道或不需要）。

## 默认 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;使用服务器默认值。

## 另请参阅 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , catalog: [:Loss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb),  [catalog::Type](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
