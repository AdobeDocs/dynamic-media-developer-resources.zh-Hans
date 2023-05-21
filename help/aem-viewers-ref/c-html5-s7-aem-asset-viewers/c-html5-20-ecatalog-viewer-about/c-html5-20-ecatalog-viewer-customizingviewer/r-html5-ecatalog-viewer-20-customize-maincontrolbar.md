---
title: 主要控制列
description: 主要控制列是桌上型電腦系統和平板電腦上的矩形區域，其中包含eCatalog檢視器可用的所有使用者介面控制項（「大頁面」按鈕除外）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 4db16599-ede0-47ae-bb5a-840655d3620b
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 1%

---

# 主要控制列{#main-control-bar}

主要控制列是桌上型電腦系統和平板電腦上的矩形區域，其中包含eCatalog檢視器可用的所有使用者介面控制項（「大頁面」按鈕除外）。

在行動電話上，它仍會保留縮圖、目錄、下載、列印、我的最愛、社交分享、全熒幕和關閉按鈕。 不過，「第一頁」和「最後一頁」按鈕以及「頁面指示器」會從主要控制列移除，並改為新增至次要控制列。 依預設，主要控制列會顯示在桌上型電腦系統和行動電話上的檢視器區域上方，並移至平板電腦上的檢視器區域下方。 它一律會採用完整的可用檢視器寬度。 您可以變更其顏色、高度和在CSS中的垂直位置（相對於檢視器容器）。

主控制列的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7controlbar`

<table id="table_2C8D322F57114A72B43053CB4539C65C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器頂端的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從檢視器底部的位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>主要控制列的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>主要控制列的背景色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**範例**  — 設定高度為36畫素且位於檢視器容器頂端的灰色主控制列。

```
.s7ecatalogviewer .s7controlbar { 
 top: 0px; 
 height: 36px; 
 background-color: rgba(0, 0, 0, 0.5); 
}
```

主控制列支援選用的捲動功能。 如果檢視器寬度太小且空間不足，無法容納控制列中預設的所有按鈕，就會啟動檢視器。 在這種情況下，控制列的右側會出現一個雙狀態箭頭按鈕。 按一下或點選此按鈕，會根據捲動按鈕的狀態，將所有控制列元素捲動至左側或右側。 此功能的主要使用案例是行動裝置，其小熒幕為直向顯示。

捲動功能在主控制列上啟用，在輔助控制列上停用。 使用下列CSS類別選取器來開啟和關閉功能：

`.s7ecatalogviewer .s7controlbar .s7innercontrolbarcontainer`

<table id="table_C8225F38309B4099AF58AA1A815A8D55"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 位置 </span> </p> </td> 
   <td colname="col2"> <p>當設定為 <span class="codeph"> 靜態 </span> 捲動功能已停用。 </p> <p>將此屬性設定為 <span class="codeph"> 絕對 </span> 以啟用捲動功能。 </p> </td> 
  </tr> 
 </tbody> 
</table>

捲動按鈕會新增至特殊容器元素，以正確放置按鈕。 它可讓您在捲動按鈕的高度小於控制列高度時，將按鈕周圍的區域與控制列背景的其餘部分設為不同的樣式。

這個捲動按鈕容器的外觀是由下列CSS類別選取器所控制：

`.s7ecatalogviewer .s7controlbar .s7scrollbuttoncontainer`

<table id="table_2CDDA8A18345497EAC4749A0D64C1658"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>通常應等於或大於捲動按鈕本身的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>容器背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以透過CSS調整捲動按鈕本身的大小和外觀。

此按鈕的外觀由下列CSS類別選取器控制：

`.s7ecatalogviewer .s7controlbar .s7scrollleftrightbutton`

<table id="table_F61CB3F696AC4018B164082FFA7777F4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕的寬度。 </p> </td> 
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
   <td colname="col2"> <p>若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 和 `selected` 屬性選取器，可將不同的外觀元素套用至不同的按鈕狀態。 尤其是， `state="selected"` 可捲動控制列內容至左側時，會對應至初始捲動按鈕狀態。 屬性 `state="default"` 與內容一直捲動至左側時的狀態相對應，而捲動按鈕會建議將其恢復為初始狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

**範例**  — 在行動電話的主控制列啟用捲動功能。 此外，設定64 x 64畫素的捲動按鈕，在選取或未選取時，針對4種不同的按鈕狀態顯示不同的影像：

```
.s7ecatalogviewer.s7size_small .s7controlbar .s7innercontrolbarcontainer { 
 position: absolute; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollbuttoncontainer { 
 width:64px; 
 background-color: rgb(0, 0, 0); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton { 
 width:64px; 
 height:64px; 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='up'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='over'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='down'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='true'][state='disabled'] { 
 background-image:url(images/v2/ControlBarLeftButton_dark_disabled_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='up'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_up_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='over'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_over_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='down'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_down_touch.png); 
} 
.s7ecatalogviewer.s7size_small.s7touchinput .s7controlbar .s7scrollleftrightbutton[selected='false'][state='disabled'] { 
 background-image:url(images/v2/ControlBarRightButton_dark_disabled_touch.png); 
}
```
