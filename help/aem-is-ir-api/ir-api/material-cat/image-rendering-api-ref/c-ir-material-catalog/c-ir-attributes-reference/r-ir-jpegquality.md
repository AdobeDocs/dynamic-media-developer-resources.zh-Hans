---
description: 默认JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。
seo-description: 默认JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。
seo-title: JpegQuality
solution: Experience Manager
title: JpegQuality
topic: Scene7 Image Serving - Image Rendering API
uuid: 82dabdae-a1f3-484a-a520-ae765914d0f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JpegQuality{#jpegquality}

默认JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。

## 属性 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整数和标记，以逗号分隔。 第一个值在1.100范围内，并定义质量。 第二个值可为0表示正常行为，或1表示禁用JPEG编码器通常采用的色度缩减采样。

## 默认 {#section-60900c0fb8c54444b2361513232514db}

如果未定义 `default::JpegQuality` 或为空，则从中继承。

## 另请参阅 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
