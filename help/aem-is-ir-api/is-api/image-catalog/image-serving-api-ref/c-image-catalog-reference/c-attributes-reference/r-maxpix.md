---
description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
seo-description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MaxPix{#maxpix}

回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。

如果请求会导致返回图像的宽度或高度大于该图像，则服务器会返回错误 `attribute::MaxPix`。

## 属性 {#section-b175425b9e9f48e0b1a71640f6a9e936}

两个大于0的整数，以逗号分隔。 宽度和高度（以像素为单位）。 也可设置为允许任 `0,0` 何无限制的回复图像大小。

## 默认 {#section-1003537434da432fb2af100ecdbf9d72}

如果未定义 `default::MaxPix` 或为空，则从中继承。

## 另请参阅 {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
