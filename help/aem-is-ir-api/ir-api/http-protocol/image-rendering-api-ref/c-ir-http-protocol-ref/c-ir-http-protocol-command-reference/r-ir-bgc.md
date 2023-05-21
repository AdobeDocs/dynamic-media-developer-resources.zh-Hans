---
title: bgc
description: 背景颜色. 指定可上色紋理和貼花的減色色彩。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9ac6517e-b9c3-48d9-97ac-d8aa65a8ba46
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 5%

---

# bgc {#bgc}

背景颜色. 指定可上色紋理和貼花的減色色彩。

`bgc= *[!DNL color]*`

<table id="simpletable_131302355CAB4900A7B45FED903A1AAD" class="- topic/simpletable "> 
 <tr class="- topic/strow strow"> 
  <td class="- topic/stentry stentry"> <p><span class="+ topic/keyword sw-d/varname varname"> color</span> </p> </td> 
  <td class="- topic/stentry stentry"> <p>RGB或灰色的值。 </p></td> 
 </tr> 
</table>

「影像演算」的紋理上色演演算法簡單明瞭 —  `bgc=` 會從紋理畫素值中減去； `color=` 最後將結果裁剪到 `0,0,0` 和 `255,255,255`.

對於紋理上色的一般用途，值 `bgc=` 可能是紋理影像中最重要或最顯著的顏色。 Dynamic Media Image Authoring提供半自動工具，可合理擷取資料 `bgc=` 來自紋理影像的顏色值。

將紋理材質套用至不可紋理化的暈映物件時， `bgc=` 套用為前景色，如果 `color=` 未指定。

## 屬性 {#section-b2db6f147d7f443ba9f671de04c2ef19}

材質屬性。 被純色和機櫃材料忽略。

## 默认 {#section-de10ef5985ee4ae1ba56d14ba8512b81}

`catalog::BaseColor` 如果材料是以目錄專案為基礎，否則 `bgc=808080` （中性灰色）。

## 示例 {#section-bf5f0f296bc448ed9d5a84afabcf81e6}

色彩化質地為主要RGB顏色120、34、193的服裝面料：

`…&src=fabrics/d213.jpg&res=40&bgc=120,34,193&color=140,95,100&…`

## 另请参阅 {#section-de9958dd63a742b4b5d780c59a57da33}

[catalog：：基本色彩](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8) ， [color=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa)
