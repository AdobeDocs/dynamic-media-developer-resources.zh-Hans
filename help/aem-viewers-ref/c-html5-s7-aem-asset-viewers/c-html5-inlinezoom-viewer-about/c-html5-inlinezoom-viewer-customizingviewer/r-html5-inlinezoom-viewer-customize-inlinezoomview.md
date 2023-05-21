---
title: 彈出式縮放檢視
description: 主檢視由靜態影像和顯示在靜態影像頂端的彈出式檢視中的縮放影像組成。 此外也包含顯示在靜態影像上方的提示訊息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 7b4b5cc9-68ad-4e7a-a2d9-3bbced929145
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '264'
ht-degree: 2%

---

# 彈出式縮放檢視{#flyout-zoom-view}

主檢視由靜態影像和顯示在靜態影像頂端的彈出式檢視中的縮放影像組成。 此外也包含顯示在靜態影像上方的提示訊息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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

提示訊息可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 以取得詳細資訊。

。

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
