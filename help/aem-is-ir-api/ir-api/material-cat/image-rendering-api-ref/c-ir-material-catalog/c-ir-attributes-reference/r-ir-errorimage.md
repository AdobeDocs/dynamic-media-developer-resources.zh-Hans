---
title: ErrorImage
description: 错误响应图像。 当发生错误时，图像渲染通常会返回带有文本消息的错误状态。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---

# ErrorImage {#errorimage}

错误响应图像。 当发生错误时，图像渲染通常会返回带有文本消息的错误状态。 的 `attribute::ErrorImage` 允许在出错时配置要返回的图像。

发生错误时，服务器会尝试解译 `ImageRendering::attribute::ErrorImage`作为简单的图像文件路径。 如果无法打开文件，则会将属性值和错误详细信息发送到图像服务，该服务将按照 `ImageServing::attribute::ErrorImage`. 如果图像服务未返回有效的响应图像，则会向客户端发送标准HTTP错误状态和文本消息。

返回错误图像，HTTP状态为200。

## 属性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字符串。 如果已指定，则必须是 **`ImageServing::catalog::id`** 值，相对路径( **`ImageServing::attribute::RootPath`** 或 **`ImageRendering::attribute::RootPath`**)，或图像服务器可访问的图像文件的绝对路径。

## 默认 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

继承自 `default::ErrorImage` 如果未定义。 如果已定义错误但为空，则即使 `default::ErrorImage` 定义，并返回HTTP错误状态。

## 另请参阅 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [属性：:ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [属性：:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [目录：:Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
