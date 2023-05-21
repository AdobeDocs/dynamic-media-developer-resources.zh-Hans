---
title: pathEmbed
description: 內嵌路徑資料。 指定回應影像中是否應包含暈映中內嵌的Photoshop路徑。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 66cc57ef-964e-4062-bb66-efeda15be744
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 2%

---

# pathEmbed{#pathembed}

內嵌路徑資料。 指定回應影像中是否應包含暈映中內嵌的Photoshop路徑。

`pathEmbed=0|1`

## 屬性 {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

要求屬性。 如果暈映不包含路徑資料則忽略。 路徑資料會縮放至 `wid=` 和/或 `hei=` 如有需要。

如果輸出影像格式不支援路徑內嵌，則忽略。 請參閱 `fmt=` 以取得支援路徑內嵌的輸出影像格式清單。

## 默认 {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`，不會將路徑內嵌在輸出影像中。

## 另请参阅 {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)， [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
