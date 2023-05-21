---
title: 我的最愛效果
description: 檢視器會在使用者最初新增該檢視的位置，在主檢視上顯示「我的最愛」圖示。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: e87226cf-56bf-4d54-8df5-91295eae90a8
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# 我的最愛效果{#favorites-effect}

檢視器會在使用者最初新增該檢視的位置，在主檢視上顯示「我的最愛」圖示。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

「我的最愛」圖示的外觀由下列CSS類別選取器控制：

```
.s7ecatalogviewer .s7favoriteseffect .s7icon
```

**最愛圖示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 為圖示顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>圖示的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 設定36 x 36畫素的最愛圖示。

```
.s7ecatalogviewer .s7favoriteseffect .s7icon { 
 height: 36px; 
 width: 36px;  
 background-image: url(images/v2/FavoriteEffect_dark_up.png); 
}
```

在桌上型電腦系統上，元件支援 `cursortype` 屬性選擇器，可套用至 `.s7favoriteseffect` 類別並根據選取的使用者動作控制游標型別。 下列專案 `cursortype` 支援的值：

<table id="table_71F8F333909247E4ACFEBDE3A1370EAB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_add </span> </p> </td> 
   <td colname="col2"> <p>顯示的使用者正在新增一個最愛圖示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_remove </span> </p> </td> 
   <td colname="col2"> <p>顯示的使用者正在移除現有的「我的最愛」圖示。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> mode_view </span> </p> </td> 
   <td colname="col2"> <p>當「我的最愛」編輯未作用中時，以正常操作模式顯示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

範例 — 針對每種元件狀態型別使用不同的滑鼠游標。

```
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_add"] { 
cursor: crosshair; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_remove"] { 
cursor: not-allowed; 
} 
.s7ecatalogviewer .s7favoriteseffect[cursortype="mode_view"] { 
cursor: auto; 
}
```
