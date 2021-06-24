---
description: 视频查看器的JavaScript API引用。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，查看器，SDK/API，视频
role: Developer,Business Practitioner
exl-id: e5d71393-fcae-4bd4-8e78-a451b2f05ffc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# setAsset{#setasset}

视频查看器的JavaScript API引用。

`setAsset(asset[, data])`

设置新资产和可选的其他资产数据。 您可以在`init()`之前或之后随时调用此参数。 如果在`init()`之后调用，则查看器在运行时会交换资产。

另请参阅[init](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字符串</span>}个新资产ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数据 </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph"> JSON </span>} JSON对象，具有以下可选字段（区分大小写）： </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph"> 后 </span> 验图像 — 在视频开始播放之前要在第一帧上显示的图像。请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph"> 题注 </span>  — 新隐藏式题注文件的位置。如果未指定文件，则用户界面中不显示隐藏式字幕按钮。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph"> 导航 </span> - WebVTT导航内容的URL或路径。WebVTT文件应由图像服务提供 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
