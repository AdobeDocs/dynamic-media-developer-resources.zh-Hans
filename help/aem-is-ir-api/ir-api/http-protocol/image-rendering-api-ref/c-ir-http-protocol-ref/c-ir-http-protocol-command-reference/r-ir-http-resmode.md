---
title: resMode
description: 重新取樣模式。 選取重新取樣和/或內插演演算法，以將演算後的影像縮放至以wid=、hei=或scl=指定的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0926dcfe-881c-4b52-b08d-c56afa0ba04d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 8%

---

# resMode{#resmode}

重新取樣模式。 選取重新取樣和/或內插補點演演算法，以將演算後的影像縮放到指定的大小 `wid=`， `hei=`，或 `scl=`.

` `resMode=bilin|bicub|sharp2|bisharp&quot;

<table id="table_AF954C101B30473FAFE9930C7B694305"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>選取標準雙線性內插。 最快的重新取样方法；某些锯齿伪影会相当明显。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>選取雙立方內插。 比雙線性內插運算耗用更多CPU，但產生更銳利的影像，且鋸齒狀不自然感更不明顯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="+ topic/ph pr-d/codeph codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>選取修改過的Lanczos視窗函式作為內插演演算法。 可能會產生比雙立方體稍微銳利的結果，但CPU成本會更高。 </p> <p> <span class="codeph"> 銳利化 </span> 已取代為 <span class="codeph"> sharp2 </span>，因此造成鋸齒狀不自然感（也稱為Moiré）的可能性較低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp </span> </p> </td> 
   <td colname="col2"> <p>選取 <span class="keyword"> Adobe Photoshop </span> 用於縮減影像大小的預設重新取樣器，在中稱為「雙立方銳利化」 <span class="keyword"> Adobe Photoshop </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-ea7029f37e094d9cb85646b85fbac0ce}

可能發生在請求中的任何位置。 若未套用最終影像縮放比例，則忽略。

## 默认 {#section-900872fb93dc41efb3e8ad5b62aadc38}

`attribute::ResMode`

## 另请参阅 {#section-16c557a2250e4f04b3e6cbef18add9ce}

[attribute：：ResMode](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-resmode.md#reference-fdca7eb6d5104fdeae9d6ac42251db82) ， [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)， [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)， [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)
