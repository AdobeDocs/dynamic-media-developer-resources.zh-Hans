---
title: illum
description: 照明地图选择器。 指定此材质希望呈现的照明映射。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# illum{#illum}

照明地图选择器。 指定此材质希望呈现的照明映射。

`illum=-1|0|1|2`

如果指定的照明映射在目标晕影中不可用，则改用最近的可用映射。

`illum=-1` 指定根据以下条件自动选择照明地图 `gloss=` 值。

## 属性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材质属性。 如果晕影未定义多个照明映射，则忽略。

## 默认 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另请参阅 {#section-9132e60381c64aa3a8ed1319690db55e}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
