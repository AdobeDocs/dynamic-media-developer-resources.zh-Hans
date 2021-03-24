---
description: 光照映射选择器。 指定此材料更喜欢用来渲染的照明映射。
solution: Experience Manager
title: 伊兰
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 4%

---


# illum{#illum}

光照映射选择器。 指定此材料更喜欢用来渲染的照明映射。

`illum=-1|0|1|2`

如果指定的照明映射在目标晕影中不可用，则使用最近的可用映射。

`illum=-1` 指定根据值自动选择照明 `gloss=` 图。

## 属性 {#section-aace8466566e4cf1a0c5a6c0167245c9}

材料属性。 如果晕影未定义多个照明映射，则忽略。

## 默认 {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## 另请参阅 {#section-9132e60381c64aa3a8ed1319690db55e}

[光泽=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
