---
title: 調色板
description: 色票由一列縮圖影像組成，其左側和右側均可選有捲動按鈕。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 7040edf2-4356-4493-b886-8c5694f5863a
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 3%

---

# 調色板{#swatches}

色票由一列縮圖影像組成，其左側和右側均可選有捲動按鈕。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

只有當所有縮圖無法符合容器的寬度時，才會在案頭上顯示捲動按鈕。 在行動裝置上，或是縮圖可符合容器寬度，則不會顯示捲動按鈕。

**色票的CSS屬性**

色票容器的外觀是由下列CSS類別選取器所控制：

```
.s7flyoutviewer .s7swatches
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 色票的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>色票的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 相對於檢視器容器的垂直色票位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要將色票設定為460 x 100畫素：

```
.s7flyoutviewer .s7swatches { 
 width: 460px; 
 height: 100px;  
}
```

**縮圖色票間距的CSS屬性**

色票縮圖之間的間距是由CSS類別選取器所控制：

```
.s7flyoutviewer .s7swatches .s7thumbcell
```

<table id="table_70FAD50E38EB4647B8FAB832F552BBB8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
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

範例 — 將間距設定為垂直和水平各為10畫素：

```
.s7flyoutviewer .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

**縮圖色票的CSS屬性**

使用下列CSS類別選取器可控制個別縮圖的外觀：

```
.s7flyoutviewer .s7swatches .s7thumb
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 縮圖色票的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖色票的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>縮圖色票的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選擇器，用於將不同的外觀元素套用至不同的縮圖狀態。 尤其是， `state="selected"` 與目前顯示在主檢視中的影像縮圖相對應， `state="default"` 對應至其餘的縮圖，以及 `state="over"` 用於滑鼠游標暫留時。

範例 — 若要設定56 x 56畫素的縮圖、淺灰色預設邊框和深灰色選取邊框：

```
.s7flyoutviewer .s7swatches .s7thumb { 
 width: 56px; 
 height: 56px;  
} 
.s7flyoutviewer .s7swatches .s7thumb[state="default"] { 
 border: 1px solid #dddddd; 
} 
.s7flyoutviewer .s7swatches .s7thumb[state="selected"] { 
 border: 1px solid #666666; 
}
```

**左右捲動按鈕的CSS屬性**

左右捲動按鈕的外觀由下列CSS類別選取器控制：

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton 
.s7flyoutviewer .s7swatches .s7scrollrightbutton
```

無法使用CSS來定位捲動按鈕 `top`， `left`， `bottom`、和 `right` 屬性。 相反地，檢視器邏輯會自動調整位置。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 捲動按鈕的寬度。 </p> </td> 
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
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#section-0711ece44a4740168cfd7624c9010bd1" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，用於將不同的外觀元素套用至按鈕狀態 `up`， `down`， `over`、和 `disabled`.

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 以取得詳細資訊。

範例 — 設定56 x 56畫素的捲動按鈕，並為每種狀態設定不同的圖稿：

```
.s7flyoutviewer .s7swatches .s7scrollleftbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="up"]{ 
background-image:url(images/v2/ScrollLeftButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="over"]{ 
 background-image:url(images/v2/ScrollLeftButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="down"]{ 
 background-image:url(images/v2/ScrollLeftButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollleftbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollLeftButton_disabled.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton { 
 background-size: auto; 
 width: 56px; 
 height: 56px; 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="up"]{ 
background-image:url(images/v2/ScrollRightButton_up.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="over"]{ 
 background-image:url(images/v2/ScrollRightButton_over.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="down"]{ 
 background-image:url(images/v2/ScrollRightButton_down.png); 
} 
.s7flyoutviewer .s7swatches .s7scrollrightbutton[state="disabled"]{ 
 background-image:url(images/v2/ScrollRightButton_disabled.png); 
}
```
