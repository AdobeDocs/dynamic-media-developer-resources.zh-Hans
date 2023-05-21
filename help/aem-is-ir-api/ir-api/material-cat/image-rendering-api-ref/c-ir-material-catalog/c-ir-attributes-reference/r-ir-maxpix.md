---
title: MaxPix
description: 回覆影像大小限制。 可傳回給使用者端的最大回覆影像寬度和高度。
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

回覆影像大小限制。 可傳回給使用者端的最大回覆影像寬度和高度。

如果請求會導致回覆影像的寬度和/或高度大於 `attribute::MaxSize`.

## 屬性 {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

兩個大於0的整數，以逗號分隔。 寬度和高度（畫素）。 亦可設為0,0，以允許任何回覆影像大小而沒有任何限制。

## 默认 {#section-45b38dc661854d11b97df5709f4f3434}

繼承自default：：MaxPix （如果未定義或為空）。

## 另请参阅 {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
