---
description: 缩览图的默认背景颜色。 用于填充不包含实际图像数据的输出缩略图图像区域的RGB值。
seo-description: 缩览图的默认背景颜色。 用于填充不包含实际图像数据的输出缩略图图像区域的RGB值。
seo-title: 缩略图BkgColor
solution: Experience Manager
title: 缩略图BkgColor
topic: Scene7 Image Serving - Image Rendering API
uuid: c75c01f4-036e-46fd-9bc1-480920c0c05a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 4%

---


# 缩略图BkgColor{#thumbbkgcolor}

缩览图的默认背景颜色。 用于填充不包含实际图像数据的输出缩略图图像区域的RGB值。

仅用于缩略图请求(`req=tmb`)以及将`catalog::ThumbType`设置为2或3时。

## 属性 {#section-a73e82c950cc4319bc3bccec14764c25}

颜色.

## 默认 {#section-b02bb56dda684ff9969806ce82ba00c2}

如果未定义或为空，则从`default::ThumbBkgColor`继承。

## 另请参阅 {#section-27983dc885424dfbba8c8e4192f3f88d}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [req=tmb](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
