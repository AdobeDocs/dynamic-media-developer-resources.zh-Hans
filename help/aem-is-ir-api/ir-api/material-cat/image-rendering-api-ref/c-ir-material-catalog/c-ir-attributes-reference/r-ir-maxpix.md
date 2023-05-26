---
title: MaxPix
description: 回复图像大小限制。 可返回到客户端的最大回复图像宽度和高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# MaxPix{#maxpix}

回复图像大小限制。 可返回到客户端的最大回复图像宽度和高度。

如果请求会导致回复图像的宽度和/或高度大于 `attribute::MaxSize`.

## 属性 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

两个大于0的整数，以逗号分隔。 宽度和高度（像素）。 也可以设置为0,0以允许使用任何回复图像大小而没有任何限制。

## 默认 {#section-45b38dc661854d11b97df5709f4f3434}

如果未定义或为空，则继承自default：：MaxPix。

## 另请参阅 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
