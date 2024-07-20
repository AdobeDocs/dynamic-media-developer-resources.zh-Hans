---
description: 缩略图的默认背景颜色。 用于填充不包含实际图像数据的输出缩略图图像的区域的RGB值。
solution: Experience Manager
title: ThumbbkgColor
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88acf5ad-2973-42f9-9aaa-901e66b07f53
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# ThumbbkgColor{#thumbbkgcolor}

缩略图的默认背景颜色。 用于填充不包含实际图像数据的输出缩略图图像的区域的RGB值。

仅用于缩略图请求(`req=tmb`)以及将`catalog::ThumbType`设置为2或3的情况。

## 属性 {#section-a73e82c950cc4319bc3bccec14764c25}

颜色。

## 默认 {#section-b02bb56dda684ff9969806ce82ba00c2}

如果未定义或为空，则从`default::ThumbBkgColor`继承。

## 另请参阅 {#section-27983dc885424dfbba8c8e4192f3f88d}

[目录：：ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ， [req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
