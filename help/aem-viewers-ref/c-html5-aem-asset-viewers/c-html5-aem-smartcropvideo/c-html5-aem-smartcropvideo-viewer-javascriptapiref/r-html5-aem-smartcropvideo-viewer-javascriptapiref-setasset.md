---
title: setAsset
description: 智能裁剪视频查看器的JavaScript API参考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 70e2a0c7-8614-432a-9e20-c6d60441bb6c
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# setAsset{#setasset}

智能裁剪视频查看器的JavaScript API参考。

`setAsset(asset[, data])`

设置新资产和可选的其他资产数据。 您可以随时在`init()`之前或之后调用此参数。 如果在`init()`之后调用，则查看器会在运行时交换资源。

另请参阅[初始化]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref\r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-e030b401b966469cb5dd121501161c2a}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">资源</span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}新资产ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">数据</span> </p> </td> 
   <td colname="col2"> <p>包含以下可选字段（区分大小写）的{ <span class="codeph"> JSON </span>} JSON对象： </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph">后影像</span> — 在视频开始播放前的第一帧显示的图像。 查看<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-cmdref/r-html5-aem-smartcropvideo-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>。 </li> 
      <li id="li_BBFF3965B69A4AC8A469FDB69097B25A"> <span class="codeph">标题</span> — 新隐藏式标题文件的位置。 如果未指定文件，则用户界面中不会显示隐藏式字幕按钮。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("Scene7SharedAssets/Glacier_Climber_MP4")
```
