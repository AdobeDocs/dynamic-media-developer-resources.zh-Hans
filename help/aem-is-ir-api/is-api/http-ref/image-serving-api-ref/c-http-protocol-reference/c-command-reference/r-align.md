---
description: 對齊影像與檢視。 在wid=和hei=定義的檢視矩形內對齊複合影像（可能是在縮放之後，如果也指定scl=）。
solution: Experience Manager
title: 對齊
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 01001cc6-1a60-4d6b-a27f-ea5822be6d11
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---

# 對齊{#align}

對齊影像與檢視。 在wid=和hei=定義的檢視矩形內對齊複合影像（可能是在縮放之後，如果也指定scl=）。

` align= *`水準圖`*, *`垂直`*`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 水準圖 </span> </span> </p> </td> 
  <td class="stentry"> <p>水準對齊方式（實數，-1.0...1.0） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 垂直 </span> </span> </p> </td> 
  <td class="stentry"> <p>垂直對齊方式（實數，-1.0...1.0） </p> </td> 
 </tr> 
</table>

指定 `align=-1,-1` 若要將複合影像的左上角與檢視的左上角對齊，請指定 `align=1,1` 將影像的右下角與檢視的右下角對齊。 對於標準影像和縮圖要求，複合影像資料未覆蓋的檢視區域會填滿 `bgc=`.

## 屬性 {#section-3fbec8206fc944eda4746d8be84f3b41}

檢視屬性。 ( `align=` 也可用來定義浮水印影像與套用浮水印之複合影像之間的對齊方式。) 無論目前的圖層設定為何，均適用。 若只有一個，則忽略 `wid=` 和 `hei=` 已指定，且 `fit=constrain` 或 `fit=stretch`.

## 默认 {#section-8a9ceff3dcc844c3af23b1c9066dac79}

`align=0,0`，可將檢視矩形中的影像置中。

## 示例 {#section-2c9447aa2e184fb8ab1a4370dc61d554}

以下請求適合 `myImage` 200x200畫素的檢視矩形。

`http://server/myRootId/myImageId?wid=200&hei=200&align=0,-1`

若 `myImage` 正方形，會填滿整個檢視矩形。 若 `myImage` 具有縱向外觀比例，縮放至200畫素高，並在檢視中水準置中。 若 `myImage` 具有橫向外觀比例，可縮放至200畫素寬，並對齊檢視的頂端邊緣。 在所有情況下，傳回的影像大小正好是200x200畫素；縮放未涵蓋的任何空間 `myImage` 填滿 `attribute::BkgColor` （指定bgc=可動態控制背景顏色）。

## 另请参阅 {#section-28b42c6db199456a800c8407faa26a99}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [浮水印](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-watermarks.md#reference-35d2c3a2c98349b792921c6cb8e73832)
