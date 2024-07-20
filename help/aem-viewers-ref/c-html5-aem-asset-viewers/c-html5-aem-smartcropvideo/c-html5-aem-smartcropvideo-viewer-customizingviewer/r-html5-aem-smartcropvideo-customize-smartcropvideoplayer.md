---
title: 视频播放器
description: 智能裁剪视频播放器是视频内容在查看器中显示的矩形区域。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 视频播放器{#video-player}

智能裁剪视频播放器是视频内容在查看器中显示的矩形区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的视频尺寸与智能裁剪视频播放器的尺寸不匹配，则视频内容将在智能裁剪视频播放器的矩形显示区域中居中。

以下CSS类选择器控制智能裁剪视频播放器的外观：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer
```

智能裁剪视频播放器的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

如果系统无法播放视频，则显示的错误消息可能会被本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

示例 — 设置智能裁切视频查看器，并将智能裁切视频播放器大小设置为512 x 288像素。

```
.s7smartcropvideoviewer .s7smartcropvideoplayer{ 
background-color: transparent; 
}
```

隐藏式字幕将放入智能裁切视频播放器内的内部容器中。 该容器的位置由支持的WebVTT定位运算符控制。 标题文本本身位于该容器中，其样式由以下CSS类选择器控制：

`. s7smartcropvideoviewer .s7videoplayer .s7caption`

隐藏式字幕的&#x200B;**CSS属性**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>隐藏式字幕文本背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>隐藏式字幕文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p> 隐藏式字幕字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p> 隐藏式字幕字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>隐藏式字幕字体。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将隐藏式字幕文本设置为14像素、浅灰色、Arial®，位于半透明的黑色背景上：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

缓冲动画的外观由以下CSS类选择器控制：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon
```

等待图标的&#x200B;**CSS属性**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 动画图标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 动画图标高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左边距</span> </p> </td> 
   <td colname="col2"> <p> 动画图标左边距，通常减去图标宽度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上边距</span> </p> </td> 
   <td colname="col2"> <p> 动画图标上边距，通常减去图标高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 旋钮艺术品。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要将缓冲动画设置为宽101像素、高29像素：

```
.s7smartcropvideoviewer .s7smartcropvideoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
