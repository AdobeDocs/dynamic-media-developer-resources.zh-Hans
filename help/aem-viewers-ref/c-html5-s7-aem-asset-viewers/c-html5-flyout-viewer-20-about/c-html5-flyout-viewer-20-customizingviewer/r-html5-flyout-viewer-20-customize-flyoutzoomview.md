---
title: 彈出式縮放檢視
description: 主檢視由靜態影像和彈出式檢視中顯示的縮放影像組成。 此外也包含顯示在靜態影像上的反白顯示導覽區域，以及顯示在靜態影像頂端的提示訊息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# 彈出式縮放檢視{#flyout-zoom-view}

主檢視由靜態影像和彈出式檢視中顯示的縮放影像組成。 此外也包含顯示在靜態影像上的反白顯示導覽區域，以及顯示在靜態影像頂端的提示訊息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在檢視的影像尺寸不符合彈出式縮放檢視的尺寸，則影像內容會置中於彈出式縮放檢視的矩形顯示區域中。

**主檢視的CSS屬性**

主檢視的外觀由下列CSS類別選取器控制：

```
.s7flyoutviewer .s7flyoutzoomview
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
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 主要檢視的背景顏色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 讓主檢視透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**彈出式檢視的CSS屬性**

彈出式檢視的外觀是由下列CSS類別選取器所控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
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
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p> 彈出檢視相對於主檢視左上角的水平位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 彈出檢視相對於主檢視左上角的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 彈出式檢視的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>彈出式檢視的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>彈出式檢視的邊框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 將彈出式檢視設定為600 x 400畫素，並在上一個範例中顯示的512 x 288主檢視右邊位移100畫素：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**主檢視中反白顯示的CSS屬性**

主要檢視中反白顯示的外觀由下列CSS類別選取器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

您可以使用CSS控制背景、邊框、透明度及類似屬性。 不過，醒目提示DOM元素的大小和位置會由檢視器邏輯管理。 不支援透過CSS覆寫它。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 反白顯示的色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> 反白顯示不透明度。 </p> <p>若為Internet Explorer 8，請使用 <span class="codeph"> 濾鏡：alpha（不透明度 — ...） )； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>邊框反白顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 若要設定透明度為40%的綠色反白顯示和一個畫素紅色邊框：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**游標的CSS屬性**

時間 `highlightmode` 引數已設為 `cursor`，反白顯示位於主檢視中以固定大小的游標圖稿取代，而此圖稿由CSS類別選取器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

您可以使用CSS控制背景影像和大小。

適用的CSS屬性包括：

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>游標圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>游標寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>游標高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>游標支援 `input` 屬性選取器，可用於針對不同裝置套用不同的游標圖稿和大小。 尤其是， `input="mouse"` 對應至桌上型電腦系統和 `input="touch"` 對應至觸控裝置。

**覆蓋圖的CSS屬性**

當 `overlay` 引數已設為 `1`，反白顯示影格或游標影像周圍的區域是由CSS類別選取器所控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>覆蓋圖顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>覆蓋不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**提示訊息的CSS屬性**

使用下列CSS類別選取器可控制提示訊息的外觀：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

您可以透過CSS設定字型樣式、大小、外觀和垂直位移。 不過，水準對齊方式是由檢視器邏輯管理。 透過CSS覆寫它，使用 `left` 或 `right` 屬性不受支援。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>從主檢視底部的位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文字色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字型名稱。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的背景填色色彩。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的背景邊框半徑。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>訊息文字的背景不透明度。 </p> <p>若為Internet Explorer 8，請使用 <span class="codeph"> 濾鏡：alpha（不透明度 — ...） ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

提示訊息可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 以取得詳細資訊。

範例 — 若要使用白色Arial® 12-px字型、距主檢視底部50畫素的位移、內距和圓角邊框來設定半透明提示訊息：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
