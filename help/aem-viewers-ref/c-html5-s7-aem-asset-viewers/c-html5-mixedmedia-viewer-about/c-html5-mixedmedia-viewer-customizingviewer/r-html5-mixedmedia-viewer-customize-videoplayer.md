---
title: 视频播放器
description: 视频播放器是视频内容在查看器中显示的矩形区域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 2f92d76e-3104-4ad8-9426-662275492251
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---

# 视频播放器{#video-player}

视频播放器是视频内容在查看器中显示的矩形区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的视频的尺寸与视频播放器的尺寸不匹配，则视频内容将在视频播放器的矩形显示区域中居中。

以下CSS类选择器控制视频播放器的外观：

```
.s7mixedmediaviewer .s7videoplayer
```

**视频播放器的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 视频播放器的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

系统无法播放视频时显示的错误消息可以本地化。 参见 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 了解更多信息。

示例 — 要使视频播放器透明，请执行以下操作：

```
.s7mixedmediaviewer .s7videoplayer { 
 background-color: transparent; 
}
```

字幕会放入视频播放器内的内部容器中。 该容器的位置由支持的WebVTT定位运算符控制。 题注文本本身位于该容器内；其样式由以下CSS类选择器控制：

```
.s7mixedmediaviewer .s7videoplayer .s7caption
```

**字幕的CSS属性**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>题注文本背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>题注文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将字幕文本设置为14像素浅灰色Arial®，请在半透明的黑色背景上设置：

```
.s7mixedmediaviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

缓冲动画的外观由以下CSS类选择器控制：

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> 左边距 </span> </p> </td> 
   <td colname="col2"> <p> 动画图标左边距，通常减去图标宽度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上边距 </span> </p> </td> 
   <td colname="col2"> <p> 动画图标上边距，通常减去图标高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p> 旋钮图稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将缓冲动画设置为宽101像素、高29像素：

```
.s7mixedmediaviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
