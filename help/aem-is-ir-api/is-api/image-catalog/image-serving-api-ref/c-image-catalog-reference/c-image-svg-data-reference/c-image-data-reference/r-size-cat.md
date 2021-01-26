---
description: 图像大小. 目录路径引用的全分辨率图像的像素大小。
seo-description: 图像大小. 目录路径引用的全分辨率图像的像素大小。
seo-title: 大小
solution: Experience Manager
title: 大小
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 11%

---


# 大小{#size}

图像大小. 目录引用的全分辨率图像的像素大小：:Path。

如果提供此值，则图像服务将使用它避免必须打开图像才能获得实际图像大小。

>[!NOTE]
>
>如果提供了`catalog::Size`，且与实际的全分辨率图像大小不同，则可能会导致未定义的行为。

## 属性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

两个整数，每个大于0，以逗号分隔。 可选。

## 默认 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果字段不存在，或该字段为空，则使用图像的实际大小。

## 另请参阅 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
