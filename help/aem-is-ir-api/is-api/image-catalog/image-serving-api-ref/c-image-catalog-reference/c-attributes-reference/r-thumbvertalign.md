---
description: 缩略图的垂直对齐方式。 指定通过wid=和hei=或属性DefaultThumbPix指定的回复图像矩形中的缩略图图像的垂直对齐方式。
solution: Experience Manager
title: ThumbVertAlign
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bb1aa398-5638-4109-bf05-bc51ace4146d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# ThumbVertAlign{#thumbvertalign}

缩略图的垂直对齐方式。 指定通过wid=和hei=或通过attribute：：DefaultThumbPix指定的回复图像矩形中的缩略图图像的垂直对齐方式。

仅用于缩略图请求( `req=tmb`)。

## 属性 {#section-f02c23248e87419caf3d95add51aea1e}

枚举。 允许的值分别为1、2和3，分别表示顶对齐、居中和底对齐。

## 默认 {#section-30caa4e772254419ad7a3a89d440666c}

继承自 `default::ThumbHorizAlign` 如果未定义或为空。

## 另请参阅 {#section-c4cd5209d994498eb56a78fcd5bbdfa4}

[目录：：ThumbType](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md) ， [attribute：：DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
