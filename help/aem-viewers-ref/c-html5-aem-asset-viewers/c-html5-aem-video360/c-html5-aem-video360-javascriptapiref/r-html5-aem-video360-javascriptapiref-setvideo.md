---
title: setvideo
description: Video360檢視器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e1894d96-6f37-4e34-a709-5b0121bd0696
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 5%

---

# setvideo{#setvideo}

Video360檢視器的JavaScript API參考

`setVideo(videoUrl)`

設定新的外部視訊。 可以隨時呼叫，無論是在之前還是之後 `init()`. 若在之後呼叫 `init()`，檢視器會在執行階段交換視訊。

另請參閱 [init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6).

## 参数 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph"> 字串</span>}新視訊的絕對URL。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Viewers/space_station_360")
```
