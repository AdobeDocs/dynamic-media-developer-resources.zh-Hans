---
title: 縮放檢檢視示效果
description: 縮放指示器覆蓋在縮放檢視區域上。 當影像處於重設狀態時會顯示它，而且它還取決於iconeffect引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: f2db0259-f1cf-41bc-86fd-97a40d01db16
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 縮放檢檢視示效果{#zoom-view-icon-effect}

縮放指示器覆蓋在縮放檢視區域上。 當影像處於重設狀態時會顯示它，而且它還取決於iconeffect引數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主要檢視器區域的CSS屬性**

檢視區域的外觀是由下列CSS類別選取器所控制：

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect
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
   <td colname="col2"> <p> 縮放指示器圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>縮放指示器高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>圖示效果支援 `media-type` 屬性選擇器，可用來將不同的圖示效果套用至不同的裝置。 尤其是， `media-type='standard'` 對應至一般使用滑鼠輸入的桌上型電腦系統，以及 `media-type='multitouch'` 對應至具有觸控輸入的裝置。

範例 — 為桌上型電腦系統和觸控裝置設定100 x 100畫素縮放指示器，使用不同的藝術品。

```
.s7mixedmediaviewer .s7zoomview .s7iconeffect { 
 width: 100px; 
 height: 100px; 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='standard'] { 
 background-image:url(images/v2/IconEffect_zoom.png); 
} 
.s7mixedmediaviewer .s7zoomview .s7iconeffect[media-type='multitouch'] { 
 background-image:url(images/v2/IconEffect_pinch.png); 
}
```
