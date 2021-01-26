---
description: 默认JPEG编码属性。 指定JPEG回复图像的默认属性。
seo-description: 默认JPEG编码属性。 指定JPEG回复图像的默认属性。
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c256c44c-2807-4a0c-b6e4-3de0a828feda
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# JpegQuality{#jpegquality}

默认JPEG编码属性。 指定JPEG回复图像的默认属性。

## 属性 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

整数数和标记，以逗号分隔。 第一个值在1.100范围内，它定义质量。 对于正常行为，第二个值可为0，或者为1以禁用JPEG编码器通常采用的RGB色度缩减采样。

## 默认 {#section-0b25eddd59bc434abfe38eeea9d45df3}

如果未定义或为空，则从`default::JpegQuality`继承。

## 另请参阅 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
