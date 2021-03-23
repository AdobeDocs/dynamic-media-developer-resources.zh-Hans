---
description: 错误响应图像。 图像渲染通常会在出现错误时返回带有文本消息的错误状态。 attribute ErrorImage允许配置要在出错时返回的图像。
seo-description: 错误响应图像。 图像渲染通常会在出现错误时返回带有文本消息的错误状态。 attribute ErrorImage允许配置要在出错时返回的图像。
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

错误响应图像。 图像渲染通常会在出现错误时返回带有文本消息的错误状态。 attribute::ErrorImage允许配置要在出错时返回的图像。

发生错误时，服务器首先尝试将`ImageRendering::attribute::ErrorImage`的值解释为简单的图像文件路径。 如果无法打开文件，它会将属性值和错误详细信息发送到图像服务，该服务将按`ImageServing::attribute::ErrorImage`中所述进行处理。 如果图像服务未返回有效的响应图像，则会将标准HTTP错误状态和文本消息发送到客户端。

返回的错误图像为HTTP状态200。

## 属性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字符串。 如果指定，则它必须是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、相对路径（**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**）或图像服务器可访问的图像文件的绝对路径。

## 默认 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

从`default::ErrorImage`继承（如果未定义）。 如果已定义错误，但为空，则即使已定义`default::ErrorImage`并返回HTTP错误状态，错误图像行为也会被禁用。

## 另请参阅 {#section-3e0308eaf4124451909dacd570e27695}

[attribute:::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
