---
title: 图标效果
description: 播放图标覆盖在主视图区域上。 它会在视频暂停或到达视频结尾时显示，并且还取决于iconeffect参数。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: e25a3b9d-88ef-4214-9b6b-2527ebf0f145
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# 图标效果{#icon-effect}

播放图标覆盖在主视图区域上。 它会在视频暂停或到达视频结尾时显示，并且还取决于iconeffect参数。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

播放图标的外观由以下CSS类选择器控制：

```
.s7video360viewer . s7video360player .s7iconeffect
```

播放图标的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 显示的播放图标图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 播放图标的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>播放图标的高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

图标效果支持`state`属性选择器。 在播放过程中暂停视频时使用属性选择器`state="play"`，在播放头位于流结尾时使用`state="replay"`。

**示例** — 设置100 x 100像素播放图标。

```
.s7video360viewer .s7videoplayer .s7iconeffect { 
 width: 100px; 
 height: 100px;} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="play"] { 
background-image: url(images/playIcon.png); 
} 
.s7video360viewer .s7videoplayer .s7iconeffect[state="replay"] { 
background-image: url(images/replayIcon.png); 
}
```
