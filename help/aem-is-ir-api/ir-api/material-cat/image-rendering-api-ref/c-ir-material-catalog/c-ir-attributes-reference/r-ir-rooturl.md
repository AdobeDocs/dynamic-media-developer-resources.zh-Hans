---
title: RootUrl
description: 相对图像URL的根URL。 指定相对图像URL的根URL。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# RootUrl{#rooturl}

相对图像URL的根URL。 指定相对图像URL的根URL。 当`attribute::RootUrl`值由`attribute::RootPath`括起来时，使用`src=`而不是{curly braces}。

## 属性 {#section-69cd0f71ea614770a8778c745d23197a}

文本字符串值。 绝对URL根路径，包括前导协议标识符。 支持以下协议：HTTP、HTTPS和FTP。

## 默认 {#section-7a81569728474725a70f3a2cc4d48e85}

如果未定义，则从`default::RootUrl`继承。 如果已定义但为空，则此材质目录不支持相对URL。

## 另请参阅 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ， `mask=`， [属性:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
