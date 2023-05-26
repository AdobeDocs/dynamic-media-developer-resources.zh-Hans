---
description: 照明地图选择器。 允许在渲染此材质时显式选择照明映射。
solution: Experience Manager
title: Illum
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e74b3e8-6289-4114-aa11-a6f91671363e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---

# Illum{#illum}

照明地图选择器。 允许在渲染此材质时显式选择照明映射。

## 属性 {#section-162bcf562ca844ccba9e81e267508cca}

枚举。 设置为–1可根据catalog：：Gloss的值自动选择照明地图。

设置为0、1或2可选择照明图A、B或C。渲染器将选择晕影中可用的最接近的照明映射。

## 默认 {#section-ac386d31ef90423b8a367010a60bddc7}

-1（自动选择）

## 另请参阅 {#section-d9db8507a5e54692b84f54b3f84b782a}

[attribute：：Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)
