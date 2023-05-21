---
title: 行动动员
description: 「呼叫動作」面板會在視訊結束時顯示，並顯示與特定視訊相關的所有互動色票。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 3%

---

# 行动动员{#call-to-action}

「呼叫動作」面板會在視訊結束時顯示，並顯示與特定視訊相關的所有互動色票。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

該面板由顯示視訊標題的標題區域、右上角的重播按鈕，以及顯示為可捲動格線的實際互動色票組成。 您可以使用來停用面板 [callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6) 設定屬性。

動作呼叫面板一律會取用整個可用的檢視器區域。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

下列CSS類別選取器會控制動作呼叫面板中背景顏色的外觀：

```
.s7interactivevideoviewer .s7calltoaction
```

## 呼叫動作面板的背景顏色的CSS屬性 {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 行動號召面板的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example}

若要設定具有深灰色背景的行動號召面板：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

下列CSS類別選擇器會控制動作呼叫面板中標題的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## 動作呼叫面板標頭的CSS屬性 {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>標題的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>頁首的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下邊框 </span> </p> </td> 
   <td colname="col2"> <p>標頭的底部邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-1}

若要設定高度為70畫素的標頭，其背景為深灰色，底部為略淺灰色的兩個畫素框線：

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

下列CSS類別選擇器會控制動作呼叫面板中標題標題的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## 行動號召面板中標題標題的CSS屬性：  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 橫幅內的文字顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> line-height </span> </p> </td> 
   <td colname="col2"> <p>行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>橫幅中文字的對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左內邊距 </span> </p> </td> 
   <td colname="col2"> <p>左內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 右內邊距，為「重播」按鈕留出空間。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-2}

若要設定具有70畫素行高、25畫素字型大小、白色和靠左對齊的視訊標題：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

下列CSS類別選擇器會控制動作呼叫面板中關閉按鈕的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## 動作呼叫面板中關閉按鈕的CSS屬性： {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>從標頭頂端的位置，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>從標頭右側的位置，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>若使用CSS拼貼，則定位在圖稿拼貼內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

## 示例 {#example-3}

若要設定28 x 28畫素的重播按鈕。 按鈕的位置必須從標頭的頂端和右側邊緣起算20畫素。 而且，它必須為四種不同按鈕狀態的每種顯示不同的影像；會從元件的Sprite影像中取得圖稿：

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

下列CSS類別選取器會控制動作呼叫面板中縮圖格線檢視的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## 行動號召面板中縮圖格線檢視的CSS屬性：  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>縮圖區域的背景色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-4}

若要設定具有深灰色背景的縮圖區域：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

下列CSS類別選擇器會控制動作呼叫面板中縮圖儲存格的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## 行動號召面板中縮圖儲存格的CSS屬性： {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍水平與垂直邊界的大小。 </p> <p>實際水準縮圖間距等於為設定的左右邊界總和 <span class="codeph"> .s7thumbcell </span>. 同樣的規則也適用於垂直間距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-5}

若要設定24畫素的水準間距和18畫素的垂直間距：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

下列CSS類別選取器會控制動作呼叫面板中縮圖的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## 行動號召面板中縮圖的CSS屬性： {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
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
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 對應於目前所選影像的縮圖； `state="default"` 對應至其餘的縮圖； `state="over"` 用於滑鼠游標暫留時。

## 示例 {#example-6}

若要設定94 x 100畫素的縮圖：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

下列CSS類別選取器會控制動作呼叫面板中縮圖示籤的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## 行動號召面板中縮圖示籤的CSS屬性： {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 標籤的文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>標籤的水準對齊方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字型系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-7}

若要設定使用白色顏色的標籤，請置中對齊15畫素，然後使用Arial®字型：

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

如果縮圖數目超過可垂直放入檢視的數目，縮圖會在右側呈現垂直卷軸。 依預設，動作呼叫面板會呈現一個沒有拇指和捲動按鈕的小垂直條。 不過，您可以變更檢視器CSS來自訂列。

下列CSS類別選擇器會控制動作呼叫面板中卷軸區域的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## 行動號召面板中卷軸區域的CSS屬性： {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 卷軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>垂直卷軸從縮圖區域頂部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>垂直卷軸從縮圖區域底部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 水準卷軸從縮圖區域的右邊緣位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-8}

若要設定寬度為22畫素的卷軸，且從縮圖區域的上方、右側或下方起沒有任何邊界，請執行下列動作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

卷軸軌跡是上下卷軸按鈕之間的區域。 元件會自動設定軌跡的位置和高度。

下列CSS類別選擇器會控制動作呼叫面板中卷軸軌跡的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## 捲動軌跡列的CSS屬性 {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>卷軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>軌跡列的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-9}

若要設定寬度為22畫素且為灰色的卷軸軌跡：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

卷軸縮圖會在捲動軌跡區域內垂直移動。 其垂直位置完全由元件邏輯控制，但縮圖高度不會隨著內容量而動態變更。

下列CSS類別選取器會控制縮圖高度和其他外觀的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## 動作呼叫面板中縮圖高度的CSS屬性： {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上內邊距 </span> </p> </td> 
   <td colname="col2"> <p>磁軌頂端之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下內邊距 </span> </p> </td> 
   <td colname="col2"> <p>軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>縮圖的顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定縮圖狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至下列不同的縮圖狀態： `"up"`， `"down"`， `"over"`、和 `"disabled"`.

## 示例 {#example-10}

若要設定卷軸縮圖，其大小為6 x 167畫素、有三個畫素圓角，且為灰色：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

下列CSS類別選取器會控制頂端和底部捲動按鈕的外觀：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

無法使用CSS top、left、bottom或right屬性來定位捲動按鈕；檢視器邏輯會自動加以定位。 互動式視訊檢視器中的動作呼叫面板不會在卷軸中使用這些按鈕，因此會在預設的CSS中將它們的大小設為0畫素。

## 行動號召面板中頂端和底部捲動按鈕的CSS屬性：  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>這些按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至下列不同的縮圖狀態： `"up"`， `"down"`， `"over"`、和 `"disabled"`.

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

## 示例 {#example-11}

將捲動按鈕的大小設為0並隱藏以停用捲動按鈕：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```
