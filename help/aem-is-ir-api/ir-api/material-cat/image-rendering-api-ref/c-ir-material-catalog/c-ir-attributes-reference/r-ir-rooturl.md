---
description: 相对图像URL的根URL。 指定相对图像URL的根URL。 当src=值由{大括号}包含时，将使用属性RootUrl而不是属性RootPath。
solution: Experience Manager
title: RootUrl *
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootUrl *{#rooturl}

相对图像URL的根URL。 指定相对图像URL的根URL。 当src=值由{大括号}括起来时，将使用attribute::RootUrl而不是attribute::RootPath。

## 属性 {#section-69cd0f71ea614770a8778c745d23197a}

文本字符串值。 绝对URL根路径，包括前导协议标识符。 支持以下协议：HTTP、HTTPS和FTP。

## 默认 {#section-7a81569728474725a70f3a2cc4d48e85}

从`default::RootUrl`继承（如果未定义）。 如果已定义但为空，则此材料目录不支持相对URL。

## 另请参阅 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
