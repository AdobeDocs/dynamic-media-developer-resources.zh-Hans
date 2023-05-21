---
description: 透視轉換。 將透視變形套用至圖層來源影像，以使用四邊形來填滿指定的區域。 圖層的其他區域仍保持透明。
solution: Experience Manager
title: 透視
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2e0297b0-c9a4-4bbd-9f06-368f722288d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 1%

---

# 透視{#perspective}

透視轉換。 將透視變形套用至圖層來源影像，以使用四邊形來填滿指定的區域。 圖層的其他區域仍保持透明。

`perspective= *`perspQuad`*[, *`resOptions`*]`

`perspectiveN= *`perspQuadN`*[, *`resOptions`*]`

<table id="simpletable_4BD38BBF53964F7D97B9E58914C97B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuad</span> </p></td> 
  <td class="stentry"> <p>透視四邊形畫素座標（8個實數，以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> perspQuadN</span> </p></td> 
  <td class="stentry"> <p>透視四邊形標準化座標（8個實數，以逗號分隔）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> resOptions</span> </p></td> 
  <td class="stentry"> <p>重新取樣選項（請參閱下文）。 </p></td> 
 </tr> 
</table>

*`perspQuad`* 由複合（或圖層0）座標空間中的四個畫素座標值組成，這些值源自複合影像的左上角。

`perspQuadN` 由四個標準化座標值組成，其中 `0.0,0.0` 對應至複合/圖層0影像的左上角，並且 `1.0,1.0` 至右下角。

轉換輸入影像，使輸入影像的左上角對應至的第一個座標值 `perspQuad[N]`，右上角至第二個座標，右下角至第三個座標，左下角至第四個座標。

>[!NOTE]
>
>`pos=` 可用來進一步定位複合影像中的轉換圖層。

透視四邊形座標可能位於複合影像的外部。

如果四邊形不適用於透視轉換（例如，如果兩個或更多頂點重合、三個或所有頂點位於同一條線上，或者四邊形是自交或凹的），則行為是未定義的。

## 品質考量 {#section-7cc9056afa614300a9b8844d39739fc3}

雖然預設實施會在品質和效能之間產生合理的折中，但有時可能需要提高來源影像的解析度來改善銳利度，或減少它以減少鋸齒狀不自然感。

如果來源是影像，請使用 `scale=` 以選擇不同的解析度（相對於影像的完整解析度）。 指定的 `scale=` 值會四捨五入至下一個較高的PTIF解析度等級。 如果是巢狀請求來源，可以調整巢狀請求產生的影像大小，以獲得所需的銳利度。 對於文字圖層，透過選取較大的size=值，同時增加指定的解析度，來調整輸入影像（演算後的文字）的解析度 `textAttr=`.

*`resOptions`* 允許選取替代的重新取樣演演算法。 支援下列值（區分大小寫）：

<table id="table_0F20007986324E228096888ED37219C0"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 值</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> R1</span> </p> </td> 
   <td> <p> 最近鄰居。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R2</span> </p> </td> 
   <td> <p> 雙線性式。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> R3</span> </p> </td> 
   <td> <p> 標準超取樣（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">R3T<span class="varname"> n</span></span> </p> </td> 
   <td> <p> 具有可調整抖動的超取樣(<span class="varname"> n</span> 必須是介於0到200之間的整數值)。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-818e57df0a1b4449888543bc6af77751}

圖層指令。 套用至目前的圖層，或套用至圖層0，如果 `layer=comp`. 被效果圖層忽略。

`res=` 當透視出現在相同圖層時，一律會被忽略。 `size=` 指定影像圖層時會略過。 `size=` 和 `res=` 在圖層中 `perspective=` 保留供日後使用。

## 默认 {#section-e35683395d514d4eb6b32924e1bf8f2f}

`None`，表示無透視轉換。

## 另请参阅 {#section-e5b71ac4a0724df6bf678dd354cfa51a}

[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b) ， [scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)， [pos=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143)， [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)
