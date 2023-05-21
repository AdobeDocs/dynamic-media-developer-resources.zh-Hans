---
title: 圖示效果
description: 迴轉指示器覆蓋在主檢視區域上。 當影像處於重設狀態時會顯示它，而且它也取決於iconeffect引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 1ded69eb-62cd-49da-ab53-124348359a58
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 2%

---

# 圖示效果{#icon-effect}

迴轉指示器覆蓋在主檢視區域上。 當影像處於重設狀態時會顯示它，而且它也取決於iconeffect引數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7spinviewer .s7spinview .s7iconeffect
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
   <td colname="col2"> <p> 迴轉指示器圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#section-b671c70acf284cb0aea678c2d2e4babc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>迴轉指示器寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>迴轉指示器高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

迴轉指示器支援 `state` 屬性選擇器，設為 `spin_1D` 如果有一維迴轉集，且 `spin_2D` 如果有多維度迴轉集。

範例 — 設定100 x 100畫素的縮放指示器。

```
.s7spinviewer .s7spinview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_1D"] { 
background-image: url(images/spinIcon_1D.png); 
} 
.s7spinviewer .s7spinview .s7iconeffect[state="spin_2D"] { 
background-image: url(images/spinIcon_2D.png); 
}
```
