---
title: 伊拉姆
description: 照明图选择器。 指定此材料希望用来渲染的照明图。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 5%

---

# 伊拉姆{#illum}

照明图选择器。 指定此材料希望用来渲染的照明图。

`illum=-1|0|1|2`

如果指定的照明图在目标晕影中不可用，则会改用最接近的可用图。

`illum=-1` 指定根据 `gloss=` 值。

## 属性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材料属性。 如果晕影未定义多个照明映射，则忽略此问题。

## 默认 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另请参阅 {#section-9132e60381c64aa3a8ed1319690db55e}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
