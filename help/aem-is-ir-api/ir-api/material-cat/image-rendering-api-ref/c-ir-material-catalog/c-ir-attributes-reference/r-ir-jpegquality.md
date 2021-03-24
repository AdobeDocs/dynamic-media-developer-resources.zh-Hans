---
description: 默认JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 4%

---


# JpegQuality{#jpegquality}

默认JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。

## 属性 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

整数数字和标志，以逗号分隔。 第一个值在1.100范围内，并定义质量。 第二个值可以是0（对于正常行为），也可以是1（用于禁用JPEG编码器通常采用的色度缩减采样）。

## 默认 {#section-60900c0fb8c54444b2361513232514db}

如果未定义或为空，则从`default::JpegQuality`继承。

## 另请参阅 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
