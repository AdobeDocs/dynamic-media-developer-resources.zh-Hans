---
title: 連結區和影像地圖
description: 在熱點最初是在AEM Assets的Dynamic Media中編寫的位置，檢視器會在主檢視上顯示熱點圖示（隨選）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 70517201-9d59-4d9c-986d-a6e9655b7956
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 2%

---

# 連結區和影像地圖{#hotspots-and-image-maps}

在熱點最初是在AEM Assets的Dynamic Media中編寫的位置，檢視器會在主檢視上顯示熱點圖示（隨選）。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

熱點圖示的外觀由下列CSS類別選擇器控制：

```
.s7carouselviewer .s7imagemapeffect .s7icon
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

<!--<a id="section_26D0B8444D1F42D493793FF54968C0B9"></a>-->

**影像地圖區域的CSS屬性**

影像地圖區域的外觀由下列CSS類別選取器控制：

`.s7carouselviewer .s7imagemapeffect .s7region`

<table id="table_DAE7A78AA4A74DC78B2D94F29E8E236B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS屬性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景 </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填色色彩。 </p> <p>指定此顏色於 <span class="codeph"> #RRGGBB </span>， <span class="codeph"> RGB(R，G，B) </span>，或 <span class="codeph"> RGBA(R，G，B，A) </span> 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>影像地圖區域填色色彩。 </p> <p>指定此顏色於 <span class="codeph"> #RRGGBB </span>， <span class="codeph"> RGB(R，G，B) </span>，或 <span class="codeph"> RGBA(R，G，B，A) </span> 格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p> 影像地圖區域邊框樣式。 應指定為" <span class="codeph"> 寬度 </span> <span class="codeph"> 純色 </span>"，其中 <span class="codeph"> 寬度 </span> 以畫素表示，並且 <span class="codeph"> 顏色 </span> 設為 <span class="codeph"> #RRGGBB </span>， <span class="codeph"> RGB(R，G，B) </span>，或 <span class="codeph"> RGBA(R，G，B，A) </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 以一個畫素的黑色邊框設定透明影像地圖區域：

```
.s7carouselviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```
