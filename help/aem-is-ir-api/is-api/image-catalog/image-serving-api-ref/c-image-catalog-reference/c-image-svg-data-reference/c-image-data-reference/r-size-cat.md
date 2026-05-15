---
description: 图像大小。 目录路径引用的全分辨率图像的像素大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
TQID: 'https://experienceleague.adobe.com/wS28XEIvINBBoYZSI-frpSbCikCyC5AhT6TyDgMsGFg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 5%

---

# 大小{#size}

图像大小。 catalog：：Path引用的全分辨率图像的像素大小。

如果提供了此值，则图像服务会使用它来避免必须打开图像才能获取实际图像大小。

>[!NOTE]
>
>如果提供了`catalog::Size`并且与实际全分辨率图像大小不同，则可能会导致未定义的行为。

## 属性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

两个整数，每个数字大于0，用逗号分隔。 可选.

## 默认 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果字段不存在，或字段为空，则使用图像的实际大小。

## 另请参阅 {#section-e63797357d5a4119a10db1e6e088f6e9}

[目录：：路径](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ， [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
