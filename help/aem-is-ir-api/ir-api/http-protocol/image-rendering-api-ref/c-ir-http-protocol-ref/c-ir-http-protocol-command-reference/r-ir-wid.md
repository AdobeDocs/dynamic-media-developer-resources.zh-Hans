---
title: wid
description: 回覆影像寬度。 指定彩現影像的縮放比例，讓回覆影像不高於指定值，同時維持影像的外觀比例。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---

# wid{#wid}

回覆影像寬度。 指定彩現影像的縮放比例，讓回覆影像不高於指定值，同時維持影像的外觀比例。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>影像寬度，以畫素為單位（整數大於0）。 </p></td> 
 </tr> 
</table>

如果兩者皆有，則不會填入影像 `wid=` 和 `hei=` 已指定且 `wid`/ `hei` 與影像的外觀比例不同。

`wid=` 和 `hei=` 共同定義伺服器傳回的影像大小。 若 `scl=` 晚於 `wid=` 或 `hei=` 在URL中，它會取消這些命令並 `scl=` 定義伺服器傳回的影像大小。

但是，如果 `wid=` 或 `hei=` 晚於 `scl=` 在URL中，他們會取消 `scl=` 和 `wid=`/ `hei=` 定義伺服器傳回的影像大小。

>[!NOTE]
>
>如果計算的或預設的回覆影像大小大於 `attribute::MaxPix`.

## 屬性 {#section-2d067c6d371748e19cb157684700a49d}

可能發生在請求中的任何位置。 調整影像大小 `wid=`， `hei=`，或 `scl=` 不會變更內嵌在回應影像中的列印解析度值。 忽略條件 `scl=` 發生於 `wid=` 或 `hei=` 在指令序列中。

## 默认 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

若 `wid=`， `hei=`，或 `scl=` 未指定，回覆影像會縮放以符合所定義的大小 `attribute::DefaultPix`. 若 `attribute::DefaultPix` 空白，則回覆影像的大小會與暈映的檢視影像相同。

## 另请参阅 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ， [attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)， [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
