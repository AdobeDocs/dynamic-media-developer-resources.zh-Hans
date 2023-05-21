---
title: 熱點
description: 在熱點最初是在AEM Assets的Dynamic Media中編寫的位置，檢視器會在主檢視上顯示熱點圖示（隨選）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: ec1d9a91-e189-470a-abe2-4f33686905e7
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 2%

---

# 熱點{#hotspots}

在熱點最初是在AEM Assets的Dynamic Media中編寫的位置，檢視器會在主檢視上顯示熱點圖示（隨選）。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

熱點圖示的外觀由下列CSS類別選擇器控制：

```
.s7interactiveimage .s7imagemapeffect .s7icon
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
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>熱點圖示圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>若使用CSS拼寫，則定位在圖稿拼寫內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>熱點圖示寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>熱點圖示高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定56 x 56畫素的熱點圖示，針對兩種不同的圖示狀態分別顯示不同的影像：

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
 width: 56px; 
 height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
 background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```
