---
title: setvideo
description: 智慧型裁切視訊檢視器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5e735e11-e359-4b98-b4a9-2c69a8eb424a
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 2%

---

# setvideo{#setvideo}

智慧型裁切視訊檢視器的JavaScript API參考

`setVideo(videoUrl[, data])`

設定新的外部視訊和選用的其他視訊資料。 可以隨時呼叫，無論是在之前還是之後 `init()`. 若在之後呼叫 `init()`，檢視器會在執行階段交換視訊。

另請參閱 [init]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 字串 </span>}新視訊的絕對URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数据 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON物件搭配下列選用欄位（區分大小寫）： </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 後方影像 </span>  — 要在視訊開始播放前的第一個影格上顯示的影像。 另請參閱 <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 註解 </span>  — 新註解檔案的位置。 如果未指定註解檔案，則註解按鈕不會顯示在使用者介面中。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph"> 導覽 </span> - WebVTT導覽內容的URL或路徑。 WebVTT檔案應該由影像伺服提供服務。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```
