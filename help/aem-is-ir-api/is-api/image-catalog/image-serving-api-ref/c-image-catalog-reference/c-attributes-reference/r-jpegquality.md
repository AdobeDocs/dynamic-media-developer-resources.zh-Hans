---
description: 默认的JPEG编码属性。 指定JPEG回复图像的默认属性。
solution: Experience Manager
title: Jpeg品质
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 3%

---

# Jpeg品质{#jpegquality}

默认的JPEG编码属性。 指定JPEG回复图像的默认属性。

## 属性 {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

用逗号分隔的整数和标志。 第一个值在1至100的范围内，用于定义质量。 对于正常行为，第二个值可以为0，或者为1以禁用JPEG编码器通常使用的RGB色度缩减采样。

## 默认 {#section-0b25eddd59bc434abfe38eeea9d45df3}

如果未定义或为空，则从`default::JpegQuality`继承。

## 另请参阅 {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
