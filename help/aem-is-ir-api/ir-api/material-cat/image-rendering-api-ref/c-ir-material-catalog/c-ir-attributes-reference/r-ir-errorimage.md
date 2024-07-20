---
title: 错误图像
description: 错误响应图像。 图像渲染通常会在发生错误时返回错误状态并显示文本消息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# 错误图像 {#errorimage}

错误响应图像。 图像渲染通常会在发生错误时返回错误状态并显示文本消息。 `attribute::ErrorImage`允许将图像配置为在发生错误时返回。

发生错误时，服务器会尝试将`ImageRendering::attribute::ErrorImage`的值解释为简单的图像文件路径。 如果无法打开该文件，则会将属性值和错误详细信息发送到图像服务，后者将按照`ImageServing::attribute::ErrorImage`中的说明进行处理。 如果图像服务未返回有效的响应图像，则会将标准HTTP错误状态和文本消息发送到客户端。

错误图像返回了HTTP状态200。

## 属性 {#section-4a4a7e37ed11483db0b9922dc68ea7db}

文本字符串。 如果指定，它必须是&#x200B;**`ImageServing::catalog::id`**&#x200B;值、相对路径（到&#x200B;**`ImageServing::attribute::RootPath`**&#x200B;或&#x200B;**`ImageRendering::attribute::RootPath`**）或图像服务器可访问的图像文件的绝对路径。

## 默认 {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

如果未定义，则从`default::ErrorImage`继承。 如果定义了该属性但为空，则会禁用错误图像行为（即使定义了`default::ErrorImage`也是如此），并返回HTTP错误状态。

## 另请参阅 {#section-3e0308eaf4124451909dacd570e27695}

[attribute：：DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)，[attribute：：ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b)，[attribute：：RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)，[catalog：：Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
