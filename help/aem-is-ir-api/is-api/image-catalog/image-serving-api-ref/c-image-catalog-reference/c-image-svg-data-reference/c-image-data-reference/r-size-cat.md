---
description: 图像大小. 目录路径引用的全分辨率图像的像素大小。
solution: Experience Manager
title: 大小
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 46f06cbb-d70f-4334-966c-624b49c3bb9b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

---

# 大小{#size}

图像大小. 目录引用的全分辨率图像的像素大小：:Path。

如果提供了此值，图像服务会使用它来避免必须打开图像才能获得实际图像大小。

>[!NOTE]
>
>如果提供了`catalog::Size`，并且与实际的全分辨率图像大小不同，则可能会导致未定义的行为。

## 属性 {#section-5c914ec8b1444a8e99d811b647cd42a3}

两个整数数字，每个大于0，用逗号分隔。 可选。

## 默认 {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

如果字段不存在，或者字段为空，则使用图像的实际大小。

## 另请参阅 {#section-e63797357d5a4119a10db1e6e088f6e9}

[catalog::Path](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) ,  [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
