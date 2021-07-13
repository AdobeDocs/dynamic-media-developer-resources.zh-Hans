---
description: 交互式视频查看器的JavaScript API引用。
solution: Experience Manager
title: setAsset
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: 24d8d11d-4688-4ca0-92ae-824a5e984a10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# setAsset{#setasset}

交互式视频查看器的JavaScript API引用。

`setAsset(asset[, data])`

设置新资产和可选的其他资产数据。 您可以在`init()`之前或之后随时调用此参数。 如果在`init()`之后调用，则查看器在运行时会交换资产。

另请参阅[init](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> asset </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="codeph">字符串</span>}个新资产ID。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 数据 </span> </p> </td> 
   <td colname="col2"> <p> { <span class="codeph"> JSON </span>} JSON对象，具有以下可选字段（区分大小写）： </p> <p> 
     <ul id="ul_924FB99ACF0F43699CD229593F1C1384"> 
      <li id="li_F3CFEF28BCB7450991EFE0BD4EB28E36"> <span class="codeph"> 后 </span> 验图像 — 在视频开始播放之前在第一帧上显示的图像。请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-videoplayer-posterimage.md#reference-8e8e2b3e7e9c4ee8b6dadf90cef494f7" format="dita" scope="local"> VideoPlayer.posterimage </a>。 </li> 
      <li id="li_D6C3E543C70942C582020780E2DF74C8"> <span class="codeph"> 题 </span> 注 — 新题注文件的位置。如果未指定，则描述按钮在用户界面中不可见。 </li> 
      <li id="li_BF866BD7275E450EA08A0E72FAA9D3AE"> <span class="codeph"> 导航 </span> - WebVTT导航内容的URL或路径。WebVTT文件应由图像服务提供。 </li> 
      <li id="li_0C0EC5AB00554EC6AA01F60684A40213"> <span class="codeph"> interactiveData  </span> - WebVTT交互式数据内容的URL或路径。WebVTT文件必须由图像服务提供。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回结果 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。

## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4")
```
