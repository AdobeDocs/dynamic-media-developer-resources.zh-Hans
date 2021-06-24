---
description: 表面粗糙度。 指定材料曲面的相对光泽度。 与“目录类型”和“目录光泽”一起使用，控制3D反射渲染效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 3%

---

# 粗糙度{#roughness}

表面粗糙度。 指定材料曲面的相对光泽度。 与catalog::Type和catalog::Gloss结合使用，可控制3D反射渲染效果。

## 属性 {#section-70c3f2394fd8477ca83a369448907971}

整数。 范围0...100中的百分比值。 适用于所有材料的可选。 仅用于具有多个反射图的晕影或具有3D反射功能的晕影。 将留空，或将其设置为–1（如果不知道或不需要）。

## 默认 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1;使用服务器默认值。

## 另请参阅 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[粗糙=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [目录：：光泽](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [目录：：类型](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
