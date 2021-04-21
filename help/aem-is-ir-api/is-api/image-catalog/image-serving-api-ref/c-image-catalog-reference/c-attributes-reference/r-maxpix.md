---
description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 3%

---


# MaxPix{#maxpix}

回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。

如果请求会导致返回图像的宽度或高度大于`attribute::MaxPix`，则服务器会返回一个错误。

## 属性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

两个大于0的整数，用逗号分隔。 宽度和高度（以像素为单位）。 也可设置为`0,0`以允许任意回复图像大小，且不受限制。

## 默认 {#section-1003537434da432fb2af100ecdbf9d72}

如果未定义或为空，则从`default::MaxPix`继承。

## 另请参阅 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
