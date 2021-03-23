---
description: 视频擦洗器是一个水平滑块控件，它允许用户动态搜索当前播放的视频中的任意时间位置。
seo-description: 视频擦洗器是一个水平滑块控件，它允许用户动态搜索当前播放的视频中的任意时间位置。
seo-title: 视频擦洗器
solution: Experience Manager
title: 视频擦洗器
uuid: c68d3693-3772-470a-893a-b701ddec3414
feature: Dynamic Media Classic，查看器，SDK/API，360 VR视频
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 2%

---


# 视频浏览条{#video-scrubber}

视频擦洗器是一个水平滑块控件，它允许用户动态搜索当前播放的视频中的任意时间位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

在播放视频时，擦洗器“旋钮”也会移动，以指示视频在播放期间的当前时间位置。 视频擦洗器始终采用控制栏的整个宽度。 可以为视频擦洗器设置皮肤。 通过CSS更改其高度和垂直位置。

通过以下CSS类选择器控制视频浏览条的常规外观：

```
.s7video360viewer .s7videoscrubber 
.s7video360viewer .s7videoscrubber .s7videotime 
.s7video360viewer .s7videoscrubber .s7knob
```

**视频浏览条的CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从上边框定位，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 从底边框中的位置，包括填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>视频擦洗器的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>视频擦洗器的颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器跟踪背景、播放和加载指示器：

```
.s7video360viewer .s7videoscrubber .s7track 
.s7video360viewer .s7videoscrubber .s7trackloaded 
.s7video360viewer .s7videoscrubber .s7trackplayed
```

**轨道的CSS属性**

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>相应轨道的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>相应轨道的颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器控制旋钮：

```
.s7video360viewer .s7videoscrubber .s7knob
```

**旋钮的CSS属性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>垂直旋钮偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>旋钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>旋钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>旋钮图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器控制播放的气泡时间：

```
.s7video360viewer .s7videoscrubber .s7videotime
```

**播放时间的CSS属性气泡**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>气泡区域宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高  </span> </p> </td> 
   <td colname="col2"> <p>气泡区域高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>气泡区域填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>气泡图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS Sprite，则位于图稿Sprite内。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 文本对齐  </span> </p> </td> 
   <td colname="col2"> <p>文本与气泡区域对齐。 </p> </td> 
  </tr> 
 </tbody> 
</table>

视频擦洗器工具提示可以本地化。 有关详细信息，请参阅[用户界面元素本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

**示例**  — 设置一个视频查看器，其中视频浏览器具有10像素高、距控件条上边缘和左边缘10像素和35像素的自定义轨道颜色。

```
.s7video360viewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7video360viewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7video360viewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7video360viewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

