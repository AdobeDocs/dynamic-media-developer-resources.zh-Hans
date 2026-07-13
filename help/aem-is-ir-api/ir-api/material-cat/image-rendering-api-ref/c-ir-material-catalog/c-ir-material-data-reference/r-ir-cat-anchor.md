---
description: 图像锚点。 指定可重复纹理、壁边框或贴花图像的锚点（热点）。
solution: Experience Manager
title: 锚点
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
TQID: 'https://experienceleague.adobe.com/-TWQdh61Hkdr81vXooodDafEwQHTMvQdSQSf--HuPIg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 3%

---

# 锚点{#anchor}

图像锚点。 指定可重复纹理、壁边框或贴花图像的锚点（热点）。

对晕影对象应用可重复的纹理，以便纹理锚点位于对象的纹理原点。 贴花图像被应用到晕影对象，使得贴花锚点位于对象的贴花原点。 对于壁边框，仅使用x值；忽略y值。

## 属性 {#section-bc4bc8b897c64535b88681e57d72942f}

用逗号分隔的两个整数。 相对于图像左上角的像素偏移。 如果`catalog::Alignment=3`和纯色和机箱材料已忽略。

## 默认 {#section-b7ccc419a356415294706cd295ae96c9}

如果字段为空或不存在，则使用可重复纹理材料的图像的左上角(0,0)，如果是贴花材料，则使用图像的中心。

## 另请参阅 {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[目录：：Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ， [锚点=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)

