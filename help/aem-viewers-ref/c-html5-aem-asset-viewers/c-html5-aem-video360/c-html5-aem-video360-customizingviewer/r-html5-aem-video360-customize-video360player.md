---
description: 视频播放器是在查看器中显示视频内容的矩形区域。
solution: Experience Manager
title: Video360播放器
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: Developer,Business Practitioner
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# Video360播放器{#video-player}

视频播放器是在查看器中显示视频内容的矩形区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的视频的尺寸与视频播放器的尺寸不匹配，则视频内容将居中在视频播放器的矩形显示区域内。

以下CSS类选择器控制视频播放器的外观：

```
.s7video360viewer .s7video360player
```

**视频播放器的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

当系统无法播放视频时，您可以将显示的错误消息本地化。

请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

示例 — 设置视频播放器大小设置为512 x 288像素的视频查看器。

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

使用以下CSS类选择器控制缓冲动画的外观：

```
.s7video360viewer .s7video360player .s7waiticon
```

**等待图标的CSS属性**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 动画图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> 动画图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 左  </span> </p> </td> 
   <td colname="col2"> <p> 动画图标左边距，通常为图标宽度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 顶部  </span> </p> </td> 
   <td colname="col2"> <p> 动画图标上边距，通常为图标高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 旋钮图稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将缓冲动画设置为101像素宽，29像素高：

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
