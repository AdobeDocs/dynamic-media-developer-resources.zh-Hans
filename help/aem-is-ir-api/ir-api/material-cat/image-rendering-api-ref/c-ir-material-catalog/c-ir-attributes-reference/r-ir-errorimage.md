---
description: 错误响应图像。 图像渲染通常会在出错时返回带有文本消息的错误状态。 属性ErrorImage允许配置在出错时要返回的图像。
seo-description: 错误响应图像。 图像渲染通常会在出错时返回带有文本消息的错误状态。 属性ErrorImage允许配置在出错时要返回的图像。
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorImage *{#errorimage}

错误响应图像。 图像渲染通常会在出错时返回带有文本消息的错误状态。 attribute:::ErrorImage允许在出错时配置要返回的图像。

发生错误时，服务器首先尝试将值解释为 `ImageRendering::attribute::ErrorImage`简单的图像文件路径。 如果无法打开文件，则会向图像服务发送属性值和错误详细信息，该服务将按中所述进行处理 `ImageServing::attribute::ErrorImage`。 如果图像服务不返回有效的响应图像，则标准HTTP错误状态和文本消息将发送到客户端。

返回的错误图像为HTTP状态200。

## 属性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字符串。 如果指定，则它必须是值、 **`ImageServing::catalog::id`** 相对路径(到或 **`ImageServing::attribute::RootPath`****`ImageRendering::attribute::RootPath`**)或图像服务器可以访问的图像文件的绝对路径。

## 默认 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

如果未定 `default::ErrorImage` 义，则从中继承。 如果已定义错误，但为空，则即使已定义错误图像行为， `default::ErrorImage` 并且返回HTTP错误状态。

## 另请参阅 {#section-3e0308eaf4124451909dacd570e27695}

[attribute:::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catalog::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
