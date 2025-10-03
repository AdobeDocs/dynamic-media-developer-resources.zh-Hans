---
title: setvideo
description: 智能裁剪视频查看器的JavaScript API参考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 5e735e11-e359-4b98-b4a9-2c69a8eb424a
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 2%

---

# setvideo{#setvideo}

智能裁剪视频查看器的JavaScript API参考

`setVideo(videoUrl[, data])`

设置新的外部视频和可选的其他视频数据。 可以在`init()`之前和之后随时调用。 如果在`init()`之后调用，则查看器会在运行时交换视频。

另请参阅[初始化]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-init.md#reference-3b570ba8b35045d6b30fb178c21a66c6)。

## 参数 {#section-b6affc90b3a84584b684641c86862e01}

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> videoUrl </span> </p> </td> 
   <td colname="col2"> <p>{<span class="codeph">字符串</span>}是指向新视频的绝对URL。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">数据</span> </p> </td> 
   <td colname="col2"> <p>包含以下可选字段（区分大小写）的{ <span class="codeph"> JSON </span>} JSON对象： </p> <p> 
     <ul id="ul_26121393BC7145FF8A43C05ACCBEFF36"> 
      <li id="li_DA50E073F3D4460CBC34243A2CBCC895"> <span class="codeph">后影像</span> — 在视频开始播放前的第一帧显示的图像。 查看<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-cmdref/r-html5-video-viewer-conf-attrib-videoplayer-posterimage.md#reference-9739abeeb9f64c02b5d2f7a0d1706103" format="dita" scope="local"> VideoPlayer.posterimage </a>。 </li> 
      <li id="li_4659E82D38EB4438AAA04FDEAF21B087"> <span class="codeph">标题</span> — 新标题文件的位置。 如果未指定题注文件，则用户界面中不会显示题注按钮。 </li> 
      <li id="li_A43A1BAB6B0F4A7981F71408F08F07D1"> <span class="codeph">导航</span> - URL或指向WebVTT导航内容的路径。 WebVTT文件应由图像服务提供服务。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

无。


## 示例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setVideo("https://s7d9.scene7.com/is/content/Scene7SharedAssets/Glacier_Climber_MP4")
```

