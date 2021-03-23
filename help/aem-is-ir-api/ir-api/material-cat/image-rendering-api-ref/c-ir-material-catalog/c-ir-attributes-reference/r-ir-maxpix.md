---
description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
seo-description: 回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---


# MaxPix{#maxpix}

回复图像大小限制。 可返回给客户端的最大回复图像宽度和高度。

如果请求会导致返回图像的宽度和/或高度大于`attribute::MaxSize`，则服务器会返回错误。

## 属性 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

两个大于0的整数，用逗号分隔。 宽度和高度（以像素为单位）。 也可设置为0,0以允许任意回复图像大小，且不受限制。

## 默认 {#section-45b38dc661854d11b97df5709f4f3434}

从默认继承：:MaxPix（如果未定义或为空）。

## 另请参阅 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
