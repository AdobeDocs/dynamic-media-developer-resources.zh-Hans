---
description: 视频播放器是在查看器中显示视频内容的矩形区域。
seo-description: 视频播放器是在查看器中显示视频内容的矩形区域。
seo-title: 视频播放器
solution: Experience Manager
title: 视频播放器
topic: Dynamic media
uuid: ff0f78b1-ff88-47b8-a118-4e0b3e75f341
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Video player{#video-player}

视频播放器是在查看器中显示视频内容的矩形区域。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在播放的视频的尺寸与视频播放器的尺寸不匹配，则视频内容将居中在视频播放器的矩形显示区域内。

以下CSS类选择器控制视频播放器的外观：

```
.s7interactivevideoviewer .s7videoplayer
```

**视频播放器的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以本地化在系统无法播放视频时显示的错误消息。

请参 [阅用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

示例——设置视频播放器大小设置为512 x 288像素的视频查看器。

```
.s7interactivevideoviewer .s7videoplayer{ 
background-color: transparent; 
}
```

隐藏式字幕将放入视频播放器内的内部容器中。 该容器的位置由支持的WebVTT定位操作员控制。 题注文本本身位于该容器中，其样式由以下CSS类选择器控制：

`.s7interactivevideoviewer .s7videoplayer .s7caption`

**隐藏字幕的CSS属性**

<table id="table_960E0D4FB91748FF9FC73C925B81879C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>隐藏式字幕文本背景。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>隐藏字幕文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体权重 </span> </p> </td> 
   <td colname="col2"> <p> 隐藏式字幕字体权重。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小 </span> </p> </td> 
   <td colname="col2"> <p> 隐藏式字幕字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列 </span> </p> </td> 
   <td colname="col2"> <p>隐藏式字幕字体。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-5b82913ff3c44b7b8187969cb15e9560}

要将隐藏式字幕文本设置为14像素、浅灰色、Arial，在半透明黑色背景上：

```
.s7interactivevideoviewer .s7videoplayer .s7caption { 
 background-color: rgba(0,0,0,0.75); 
 color: #e6e6e6; 
 font-weight: normal; 
 font-size: 14px; 
 font-family: Arial,Helvetica,sans-serif; 
}
```

缓冲动画的外观由以下CSS类选择器控制：

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon
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
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p> 动画图标左边距，通常为图标宽度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p> 动画图标上边距，通常为图标高度的一半。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像 </span> </p> </td> 
   <td colname="col2"> <p> 旋钮图稿。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——将缓冲动画设置为宽101像素、高29像素：

```
.s7interactivevideoviewer .s7videoplayer .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```

