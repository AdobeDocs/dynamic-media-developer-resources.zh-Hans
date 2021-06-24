---
description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# MaxPix{#maxpix}

回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。

如果请求会导致返回图像的宽度或高度大于`attribute::MaxPix`，则服务器会返回错误。

## 属性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

两个大于0的整数，用逗号分隔。 宽度和高度（以像素为单位）。 也可以将设置为`0,0`以允许任何无限制的回复图像大小。

## 默认 {#section-1003537434da432fb2af100ecdbf9d72}

从`default::MaxPix`继承（如果未定义或为空）。

## 另请参阅 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
