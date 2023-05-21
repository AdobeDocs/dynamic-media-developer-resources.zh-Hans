---
title: 互動色票
description: 如果在設定中將互動式資料傳遞給檢視器，互動式色票面板會顯示在視訊內容旁邊。 它由頂端的橫幅組成，可轉譯「按一下即可檢視」等文字、一欄中的一或多個互動色票和兩個捲動按鈕（僅適用於案頭系統）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---

# 互動色票{#interactive-swatches}

如果在設定中將互動式資料傳遞給檢視器，互動式色票面板會顯示在視訊內容旁邊。 它由頂端的橫幅組成，可轉譯「按一下即可檢視」等文字、一欄中的一或多個互動色票和兩個捲動按鈕（僅適用於案頭系統）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

在桌上型電腦系統和觸控裝置上，互動式色票會以橫向呈現，並垂直呈現在視訊內容的右側。 在觸控裝置上，會以直向方式顯示在檢視器底部，形成水準排的色票。

下列CSS類別選取器可控制互動式色票面板的位置和方向：

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 互動色票的CSS屬性 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的寬度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的頂端位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的底部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的左側位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>互動式色票面板的右方位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

互動式色票面板的執行階段位置和方向是由上述CSS屬性的組合所定義，如下所示：

* 若要在檢視器底部水準彩現互動色票，請將高度設定為絕對畫素值；將左右設定為0px；將寬度、右上設定為auto。
* 若要在視訊內容右方垂直彩現互動色票，請將寬度設定為絕對畫素；將右上角設定為0px；將高度設定為auto，將左下角設定為auto。

可以搭配此樣式使用CSS標籤，以最適化地放置互動式色票面板。

## 示例 {#example}

若要設定互動式色票面板，在橫向觸控裝置上，在檢視器底部水準彩現。 此外，若要在所有其他情況下垂直顯示在視訊內容的右側，請執行下列動作：

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

橫幅的大小和位置由互動式色票元件根據其他套用CSS的樣式來管理，且無法明確設定。

下列CSS類別選擇器會控制橫幅面板的外觀：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 橫幅面板的CSS屬性 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內的文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板周圍的邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內文字使用的字型粗細。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內文字使用的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內文字所使用的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>橫幅面板內文字使用的字型對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

橫幅工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

若要設定具有深灰色背景、淺灰色雙畫素邊框和白色文字水準置中的橫幅：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

下列CSS類別選取器會控制色票的外觀：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## 色票區域的CSS屬性 {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>色票區域的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-9cadd62a09fd44a280f55ff42437e416}

若要設定具有深灰色背景的色票區域：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

下列CSS類別選取器會控制色票縮圖之間的間距：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 色票縮圖間距的CSS屬性 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍水平與垂直邊界的大小。 實際縮圖間距等於為設定的左右邊界總和 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

若要將垂直間距設定為10畫素：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

下列CSS類別選取器可控制個別縮圖的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 個別縮圖外觀的CSS屬性 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>縮圖的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選取器，可用來將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 對應於目前所選影像的縮圖； `state="default"` 對應至其餘的縮圖； `state="over"` 用於滑鼠游標暫留時。

## 示例 {#section-69fec189ffaa440b97b6b846c320b75b}

若要設定100 x 75畫素的縮圖：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

下列CSS類別選取器會控制縮圖示籤的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## 縮圖示籤外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>標籤邊框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>水準文字對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-eb141eb6c1154183baa69796edb90536}

若要設定標籤以使用左對齊、白色、12畫素、Helvetica®字型和底部框線：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

下列CSS類別選取器可控制向上和向下捲動按鈕的外觀：

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

無法使用CSS來定位捲動按鈕 `top`， `left`， `bottom`、和 `right` 屬性；相反地，檢視器邏輯會自動將其定位。

## 上下捲動按鈕外觀的CSS屬性 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>捲動按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>圖稿sprite內的位置（如果使用CSSsprite）。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選取器，可用來將不同的外觀元素套用至按鈕狀態： 」 `up`「， 」 `down`「， 」 `over`「和」 `disabled`「。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

## 示例 {#section-e6ce4fa084b84288bc7583342b2c510c}

若要設定向上捲動按鈕（60 x 36畫素），請針對每個狀態使用不同的圖稿，並從元件的Sprite影像中取得該圖稿：

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
