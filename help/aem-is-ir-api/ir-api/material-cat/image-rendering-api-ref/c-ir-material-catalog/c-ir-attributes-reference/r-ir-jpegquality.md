---
title: Jpeg品质
description: 默认的JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 3%

---

# Jpeg品质{#jpegquality}

默认的JPEG编码质量。 指定JPEG编码的回复图像的默认质量设置。

## 属性 {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

用逗号分隔的整数和标志。 第一个值在1至100的范围内，用于定义质量。 对于正常行为，第二个值可以是`0`，或者可以是`1`以禁用JPEG编码器采用的色度缩减采样。

## 默认 {#section-60900c0fb8c54444b2361513232514db}

如果未定义或为空，则从`default::JpegQuality`继承。

## 另请参阅 {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
