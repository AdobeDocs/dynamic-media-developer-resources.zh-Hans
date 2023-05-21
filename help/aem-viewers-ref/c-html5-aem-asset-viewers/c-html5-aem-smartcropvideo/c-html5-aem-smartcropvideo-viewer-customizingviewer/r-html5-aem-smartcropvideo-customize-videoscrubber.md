---
title: 視訊筆畫壓感
description: 視訊筆畫壓感是水準滑桿控制項，可讓使用者動態搜尋目前播放視訊內的任何時間位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 9f7e3fec-8303-4114-86b2-fb75d041701d
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 3%

---

# 視訊筆畫壓感{#video-scrubber}

視訊筆畫壓感是水準滑桿控制項，可讓使用者動態搜尋目前播放視訊內的任何時間位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

清除器「旋鈕」也會隨著視訊播放而移動，以指出視訊在播放期間的目前時間位置。 視訊筆畫壓感一律採用控制列的整個寬度。 您可以透過CSS建立視訊筆畫壓感的外觀、變更其高度和垂直位置。

視訊筆畫壓感的一般外觀是由下列CSS類別選取器所控制：

```
.s7smartcropvideoviewer .s7videoscrubber 
.s7smartcropvideoviewer .s7videoscrubber .s7videotime 
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**視訊筆畫壓感的CSS屬性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>上邊框的位置，包括邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 從下邊框定位，包括內距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>視訊清除程式的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>視訊筆畫壓感色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選取器會追蹤背景、播放和載入指標：

```
.s7smartcropvideoviewer .s7videoscrubber .s7track 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed
```

**曲目的CSS屬性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>對應軌道的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>對應曲目的色彩。 </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器會控制旋鈕：

```
.s7smartcropvideoviewer .s7videoscrubber .s7knob
```

**旋鈕的CSS屬性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>垂直旋鈕位移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>旋鈕寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>旋鈕高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>旋鈕圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

下列CSS類別選擇器可控制播放時間泡泡：

```
.s7smartcropvideoviewer .s7videoscrubber .s7videotime
```

**時間播放泡泡的CSS屬性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 用於時間顯示文字的字型顏色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域寬度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>泡泡區域邊框間距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>泡泡圖稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p> 若使用CSS sprite，則定位在圖稿sprite內。 </p> <p>另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-customizingviewer/c-html5-aem-smartcropvideo-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS精靈 </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>文字與泡泡區域的對齊方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

視訊筆畫壓感工具提示可以本地化。 另請參閱 [使用者介面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad) 以取得詳細資訊。

**範例**  — 若要設定含有自訂軌跡顏色（10畫素高）之視訊筆畫壓感的視訊檢視器。 最後，請讓它位於距離控制列上邊緣和左邊緣10畫素和35畫素的位置。

```
.s7smartcropvideoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7smartcropvideoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
