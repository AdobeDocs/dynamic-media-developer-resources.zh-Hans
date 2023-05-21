---
title: setAsset
description: 互動式視訊檢視器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# setAsset{#setasset}

互動式視訊檢視器的JavaScript API參考。

`setAsset(asset[, data])`

設定新資產和選用的其他資產資料。 您可以隨時在之前或之後呼叫此引數 `init()`. 如果是在之後呼叫 `init()`，檢視器會在執行階段交換資產。

另請參閱 [init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b).

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> 字串 </span>}個新資產ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数据 </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON物件搭配下列選用欄位（區分大小寫）： </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> 後方影像 </span>  — 要在視訊開始播放前的第一個影格上顯示的影像。 另請參閱 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>. </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> 註解 </span>  — 新註解檔案的位置。 如果未指定，則不會在使用者介面中顯示註解按鈕。 </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> 導覽 </span> - WebVTT導覽內容的URL或路徑。 WebVTT檔案應該由影像伺服提供服務。 </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData </span> - WebVTT互動式資料內容的URL或路徑。 WebVTT檔案必須由影像伺服提供服務。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
