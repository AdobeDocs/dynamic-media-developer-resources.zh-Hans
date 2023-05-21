---
title: setAsset
description: 智慧型裁切視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 70e2a0c7-8614-432a-9e20-c6d60441bb6c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 3%

---

# setAsset{#setasset}

智慧型裁切視訊檢視器的JavaScript API參考。

`setAsset(asset[, data])`

設定新資產和選用的其他資產資料。 您可以隨時在之前或之後呼叫此引數 `init()`. 如果是在之後呼叫 `init()`，檢視器會在執行階段交換資產。

另請參閱 [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 字串 </span>}個新資產ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数据 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON物件搭配下列選用欄位（區分大小寫）： </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 後方影像 </span>  — 要在視訊開始播放前的第一個影格上顯示的影像。 另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 註解 </span>  — 新隱藏式字幕檔案的位置。 如果未指定檔案，則使用者介面中不會顯示隱藏式字幕按鈕。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
