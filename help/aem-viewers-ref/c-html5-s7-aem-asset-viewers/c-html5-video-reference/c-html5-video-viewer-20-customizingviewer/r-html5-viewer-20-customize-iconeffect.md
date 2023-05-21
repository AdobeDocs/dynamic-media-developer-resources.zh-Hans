---
title: 圖示效果
description: 播放圖示覆蓋在主檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，也會取決於iconeffect引數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: f4bf343a-4a78-470b-abe5-94e2d608f45d
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# 圖示效果{#icon-effect}

播放圖示覆蓋在主檢視區域上。 它會在視訊暫停或到達視訊結尾時顯示，也會取決於iconeffect引數。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放圖示的外觀由下列CSS類別選取器控制：

```
.s7videoviewer . s7videoplayer .s7iconeffect
```

**播放圖示的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 播放圖示顯示的影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 播放圖示的寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>播放圖示的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

圖示效果支援 `state` 屬性選擇器。 時間 `state="play"` 在播放期間暫停視訊時使用，並且 `state="replay"` 當播放點位於資料流結尾時使用。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

設定100 x 100畫素播放圖示。

```
.s7videoviewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7videoviewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
