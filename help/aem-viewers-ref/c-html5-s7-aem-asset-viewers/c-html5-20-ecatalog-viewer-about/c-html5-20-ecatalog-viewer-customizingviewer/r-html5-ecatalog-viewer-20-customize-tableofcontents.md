---
title: 目录
description: 目錄是位於主控制列中的按鈕。 啟動後，下拉式面板隨即顯示，內含頁面索引和標籤清單。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 9b61e269-201d-4083-9c47-0b73d55aa6ed
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '1061'
ht-degree: 2%

---

# 目录{#table-of-contents}

目錄是位於主控制列中的按鈕。 啟動後，下拉式面板隨即顯示，內含頁面索引和標籤清單。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

根據設定，清單可包含目錄中存在的所有頁面，或僅包含已定義明確標籤的頁面。 在案頭系統上，如果清單比可用的熒幕空間長，右側會顯示卷軸。

檢視器使用者介面中目錄按鈕的位置和大小由以下CSS類別選取器控制：

```
.s7ecatalogviewer .s7tableofcontents
```

**目錄的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 頂端邊界 </span> </p> </td> 
   <td colname="col2"> <p> 從控制列頂端的位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左邊界 </span> </p> </td> 
   <td colname="col2"> <p> 與左側或控制列左側的下一個按鈕（如果它是列中的第一個按鈕）的距離。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 目錄按鈕的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 目錄按鈕的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按鈕支援 `state` 屬性選擇器，可將不同的外觀元素套用至不同的按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

範例 — 設定目錄按鈕，此按鈕的位置從底部算起4畫素，從主控制列左側算起43畫素。 大小為28 x 28畫素，而且會針對四種不同的按鈕狀態分別顯示不同的影像：

```
.s7ecatalogviewer .s7tableofcontents { 
margin-top: 4px; 
margin-left: 10px; width: 28px; 
 height: 28px; 
} 
.s7ecatalogviewer .s7tableofcontents[state='up'] { 
background-image:url(images/v2/TableOfContents_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='over'] { 
background-image:url(images/v2/TableOfContents_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='down'] { 
background-image:url(images/v2/TableOfContents_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents[state='disabled'] { 
background-image:url(images/v2/TableOfContents_dark_disabled.png); 
}
```

下拉式面板的外觀由下列CSS類別選取器控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel
```

**下拉式面板的CSS屬性**

<table id="table_A18B6978EC304C378F5FE92DD44D138D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 下拉式面板的背景顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 面板邊界與內容之間的內部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> box-shadow </span> </p> </td> 
   <td colname="col2"> <p> 面板周圍的陰影。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>無法從CSS控制下拉式面板的大小或位置；元件會以程式設計方式管理其版面。

範例 — 設定具有半透明黑色背景、內容周圍5個畫素邊界和陰影的下拉式面板：

```
.s7ecatalogviewer .s7tableofcontents .s7panel { 
 background-color: rgba(0, 0, 0, 0.5); 
 margin: 5px; 
 box-shadow: 2px 2px 3px #c0c0c0; 
}
```

個別專案的外觀和使用下列CSS類別選擇器控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7item
```

**專案的CSS屬性**

<table id="table_86E777A5851F47D6A49D966E24A9A6CD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>專案的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>內部內距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>下拉式清單專案支援 `state` 屬性選取器，可將不同的外觀元素套用至暫留和選取的專案狀態。

範例 — 設定Helvetica® 14畫素字型和19畫素高的下拉式清單專案。 當選取時，專案在暫留時具有深灰色背景，且具有淺灰色背景：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item { 
font-family: Helvetica,sans-serif; 
font-size: 14px; 
height: 19px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="over"] { 
background-color: rgb(102, 102, 102); 
} 
.s7ecatalogviewer .s7tableofcontents .s7panel .s7item[state="selected"] { 
background-color: rgb(178, 178, 178); 
}
```

顯示頁面索引的元素是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index
```

**頁面索引的CSS屬性**

<table id="table_FAA5072E4AAC48F4BE00B05D87FD9827"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> 最小元素寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> 最大元素寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 頁面索引和頁面標籤之間的距離。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>您可以透過設定來完全隱藏頁面索引 `display:none` 的 `s7index` CSS類別。

範例1 — 設定最小寬度為40畫素的頁面索引、最大寬度為70畫素的頁面索引，以及右側的5畫素邊界：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
max-width: 70px; 
min-width: 40px; 
padding-right: 5px; 
}
```

範例2 — 隱藏頁面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7index { 
display: none; 
}
```

頁面標籤是由下列CSS類別選擇器所控制：

```
 .s7ecatalogviewer .s7tableofcontents .s7panel .s7label
```

**頁面標籤的CSS屬性**

<table id="table_A42E372D931D4F04855EE5AB5530CB12"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> min-width </span> </p> </td> 
   <td colname="col2"> <p> 最小元素寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> max-width </span> </p> </td> 
   <td colname="col2"> <p> 最大元素寬度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定最小寬度為40畫素和最大寬度為240畫素的頁面索引：

```
.s7ecatalogviewer .s7tableofcontents .s7panel .s7label { 
min-width: 40px; 
max-width: 240px; 
}
```

如果下拉式面板中的專案數量無法垂直放置，且系統為桌上型電腦，則元件會在面板右側呈現垂直卷軸。 卷軸區域的外觀是由下列CSS類別選取器所控制：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar
```

**卷軸的CSS屬性**

<table id="table_D34A63AAE6324699ABDCC08355D33035"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 卷軸寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 垂直卷軸從面板區域頂部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 垂直卷軸從面板區域的底部位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 水準卷軸從面板區域的右邊緣位移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定寬度為28畫素的卷軸，且面板的頂端、右側或底部區域沒有邊界：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:28px; 
}
```

卷軸軌跡是上下捲動按鈕之間的區域。 元件會自動設定軌跡的位置和高度。 使用下列CSS類別選取器來控制曲目：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack
```

**捲動軌跡的CSS屬性**

<table id="table_E49EE04B3FF64AB2948E7C09DF3EA1B7"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>磁軌寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>軌跡背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定寬度為28畫素且具有半透明灰色背景的卷軸軌跡：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolltrack { 
 width:28px; 
 background-color:rgba(102, 102, 102, 0.5); 
}
```

卷軸縮圖會在捲動軌跡區域內垂直移動。 其垂直位置是由元件邏輯所控制。 不過，縮圖高度不會隨著內容量而動態變更。 您可以使用以下CSS類別選取器來設定縮圖高度和其他方面：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb
```

**卷軸縮圖的CSS屬性**

<table id="table_D8DFBC2419BD4AB3B4892AC7B599C70A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮圖寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮圖高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上內邊距 </span> </p> </td> 
   <td colname="col2"> <p> 磁軌頂端之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 下內邊距 </span> </p> </td> 
   <td colname="col2"> <p>軌道底部之間的垂直邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定縮圖狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>縮圖支援 `state` 屬性選取器，可將不同的外觀元素套用至 `up`， `down`， `over`、和 `disabled` 縮圖狀態。

範例 — 設定一個卷軸縮圖，其大小為28 x 45畫素，頂端和底部有10畫素邊界，且每個狀態都有不同的圖稿：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb { 
 width:28px; 
 background-repeat:no-repeat; 
 background-position:center; 
 height:45px; 
 padding-top:10px; 
 padding-bottom:10px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollthumb[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollThumb_dark_up.png); 
}
```

上下捲動按鈕的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton
```

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton
```

無法使用CSS來定位捲動按鈕 `top`， `left`， `bottom`、和 `right` 屬性；相反地，檢視器邏輯會自動將其定位。

**向上捲動和向下捲動按鈕的CSS屬性**

<table id="table_89561098E43D44C2865267687BBF38F4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>按鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 針對指定按鈕狀態顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>按鈕支援 `state` 屬性選取器，可將不同的外觀元素套用至 `up`， `down`， `over`、和 `disabled` 按鈕狀態。

按鈕工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 以取得詳細資訊。

範例 — 設定28 x 32畫素的捲動按鈕，並為每種狀態設定不同的圖稿：

```
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrollupbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollUpButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton { 
 width:28px; 
 height:32px; 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='up'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='over'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_over.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='down'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_down.png); 
} 
.s7ecatalogviewer .s7tableofcontents .s7scrollbar .s7scrolldownbutton[state='disabled'] { 
 background-image:url(images/v2/ThumbnailScrollDownButton_dark_up.png); 
}
```
