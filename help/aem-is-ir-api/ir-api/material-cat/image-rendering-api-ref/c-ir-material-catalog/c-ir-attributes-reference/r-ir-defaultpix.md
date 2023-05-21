---
title: 預設畫素
description: 預設演算影像大小。 如果要求未使用wid=或hei=明確指定檢視大小，伺服器會將回覆影像限製為不得大於此寬度與高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---

# 預設畫素{#defaultpix}

預設演算影像大小。 如果要求未使用wid=或hei=明確指定檢視大小，伺服器會將回覆影像限製為不得大於此寬度與高度。

## 屬性 {#section-9dc5474fc75842308796ab6440b29611}

0或更大的兩個整數，以逗號分隔。 寬度和高度（畫素）。 可將任一或兩個值都設定為0，以保持其不受限制。

不適用於巢狀/內嵌請求。

## 默认 {#section-1935781c561e4679aa87a5bcced8df90}

繼承自 `default::DefaultPix` 如果未定義或為空。

## 另请参阅 {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
