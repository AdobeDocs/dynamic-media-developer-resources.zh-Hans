---
description: 缩览图的水平对齐。 指定由wid=和hei=或属性DefaultThumbPix指定的回复图像矩形中缩览图图像的水平对齐方式。
solution: Experience Manager
title: 缩略图对齐
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

---


# ThumbHorizAlign{#thumbhorizalign}

缩览图的水平对齐。 指定由wid=和hei=或by attribute::DefaultThumbPix指定的回复图像矩形中缩略图的水平对齐方式。

仅用于缩略图请求(`req=tmb`)。

## 属性 {#section-c98f793986cd4f98a3995615e3b68f76}

枚举。 允许的值分别为1、2和3，分别用于左对齐、居中对齐和右对齐。

## 默认 {#section-0c06f0d998cb4306868b360a06c32e5b}

如果未定义或为空，则从`default::ThumbHorizAlign`继承。

## 另请参阅 {#section-a74a13c3643140cf971d7a4275e0fdb3}

[catalog::ThumbType](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [attribute::DefaultThumbPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultthumbpix.md#reference-cf52bb74bed2466e8bc8adb0cacd6141),  [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47),  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
