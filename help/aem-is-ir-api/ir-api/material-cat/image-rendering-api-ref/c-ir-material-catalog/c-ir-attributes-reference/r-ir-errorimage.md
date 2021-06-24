---
description: 错误响应图像。 当发生错误时，图像渲染通常会返回带有文本消息的错误状态。 属性ErrorImage允许配置出错时要返回的图像。
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---

# ErrorImage *{#errorimage}

错误响应图像。 当发生错误时，图像渲染通常会返回带有文本消息的错误状态。 attribute::ErrorImage允许配置出错时要返回的图像。

发生错误时，服务器首先尝试将`ImageRendering::attribute::ErrorImage`的值解释为简单的图像文件路径。 如果无法打开文件，则会向图像服务发送属性值和错误详细信息，图像服务将按照`ImageServing::attribute::ErrorImage`中的说明进行处理。 如果图像服务未返回有效的响应图像，则会向客户端发送标准HTTP错误状态和文本消息。

返回错误图像，HTTP状态为200。

## 属性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字符串。 如果指定，则必须是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、相对路径（到&#x200B;**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**）或图像服务器可访问的图像文件的绝对路径。

## 默认 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

从`default::ErrorImage`继承（如果未定义）。 如果已定义错误但为空，则即使定义了`default::ErrorImage`并返回HTTP错误状态，错误图像行为也会被禁用。

## 另请参阅 {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
