---
description: 表面粗糙度。 指定材料曲面的相对光泽度。 与目录“类型”和目录“光泽”一起使用可控制3D反射渲染效果。
solution: Experience Manager
title: 粗糙度
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
TQID: 'https://experienceleague.adobe.com/YvUmUkOLzzbM7Zs-7T35rwYRNrUeh6-QXW339AA3R8Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 2%

---

# 粗糙度{#roughness}

表面粗糙度。 指定材料曲面的相对光泽度。 与catalog：：Type和catalog：：Gloss一起使用可控制3D反射渲染效果。

## 属性 {#section-70c3f2394fd8477ca83a369448907971}

整数。 介于0和100之间的百分比值。 对于所有材料而言，它是可选的。 仅用于具有多个反射映射的晕影或具有3D反射功能的晕影。 留空或设置为–1 （如果不知道或不需要它）。

## 默认 {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1；使用服务器缺省值。

## 另请参阅 {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[rough=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) ，[目录：：Gloss](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb)，[目录：：类型](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

