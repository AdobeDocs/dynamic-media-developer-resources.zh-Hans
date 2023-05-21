---
title: 色票
description: 色票包含一列縮圖影像，且左側和右側均可選用捲動按鈕。 只有在所有縮圖無法符合容器寬度時，才會在案頭上顯示色票。 在行動裝置上，或是縮圖可符合容器寬度，則不會顯示捲動按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0a73d1c9-362d-48a5-96c9-3d543e68ebec
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 3%

---

# 色票{#color-swatches}

色票包含一列縮圖影像，且左側和右側均可選用捲動按鈕。 只有在所有縮圖無法符合容器寬度時，才會在案頭上顯示色票。 在行動裝置上，或是縮圖可符合容器寬度，則不會顯示捲動按鈕。

色票容器的外觀是由CSS類別選取器所控制：

```
.s7mixedmediaviewer .s7colorswatches .s7swatches
```

**色票的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>色票的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>色票的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>相對於檢視器容器的垂直色票位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定高度為100畫素的色票。

```
.s7mixedmediviewer .s7colorswatches .s7swatches { 
 height: 100px;  
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

色票縮圖之間的間距由下列CSS類別選取器控制：

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumbcell`

<table id="table_ECE063DB98154E099FB024F66FF877D7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每個縮圖周圍水平與垂直邊界的大小。 實際縮圖間距等於為設定的左右邊界總和 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例**

將間距設定為十畫素（垂直和水平）。

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

使用下列CSS類別選取器可控制個別縮圖的外觀：

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
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
>縮圖支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 與目前顯示在主檢視中的影像縮圖相對應， `state="default"` 對應至其餘的縮圖，以及 `state="over"` 用於滑鼠游標暫留時。

範例 — 設定56 x 56畫素的縮圖，其預設邊框為淺灰色，選取邊框為深灰色。

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7mixedviewer .s7colorswatches .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

左右捲動按鈕的外觀由下列CSS類別選取器控制：

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton`

`.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton`

無法使用CSS來定位捲動按鈕 `top`， `left`， `bottom`、和 `right` 屬性。 相反地，檢視器邏輯會自動調整位置。

<table id="table_A5663C4AAC4446168CAD8DBA2894BB9C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態： `up`， `down`， `over`、和 `disabled`.

範例 — 設定56 x 56畫素的捲動按鈕，每個狀態都有不同的圖稿。

```
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7mixedmediaviewer .s7colorswatches .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
