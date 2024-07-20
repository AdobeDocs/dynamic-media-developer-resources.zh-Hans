---
title: 视频洗刷
description: 视频洗刷是水平滑块控件，允许用户动态搜索到当前播放视频内的任何时间位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 3e9c8800-fda2-41d1-8436-b2de7952652c
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---

# 视频洗刷{#video-scrubber}

视频洗刷是水平滑块控件，允许用户动态搜索到当前播放视频内的任何时间位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

清理器“旋钮”也会在视频播放时移动，以指示视频在播放期间的当前时间位置。 视频清理器始终占据控制栏的全部宽度。 可以使用CSS为视频洗刷蒙皮，并更改其高度和垂直位置。

视频清理器的常规外观由以下CSS类选择器控制：

```
.s7mixedmediaviewer .s7videoscrubber 
.s7mixedmediaviewer .s7videoscrubber .s7videotime 
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

视频清理器的&#x200B;**CSS属性**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>上边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p> 下边框的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>视频洗刷的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>视频洗刷的颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器跟踪背景、播放和加载指示器：

```
.s7mixedmediaviewer .s7videoscrubber .s7track 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed
```

曲目&#x200B;**的** CSS属性

<table id="table_46903DCACF314426B67783167ADF7715"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>相应轨道的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>相应轨道的颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器控制旋钮：

```
.s7mixedmediaviewer .s7videoscrubber .s7knob
```

旋钮的&#x200B;**CSS属性**

<table id="table_966826FB81114362A8D81D1EED38D512"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>垂直旋钮偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>旋钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>旋钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>旋钮艺术品。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器控制播放时间气泡：

```
.s7mixedmediaviewer .s7videoscrubber .s7videotime
```

播放时间泡泡的&#x200B;**CSS属性**

<table id="table_21E9AD3FBC8C4437BA02E5CD1BF7E831"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p> 用于时间显示文本的字体颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>气泡区域宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>气泡区域高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>气泡区域边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>气泡图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#section-209a43dfbddf4fc589e79cddaf233f50" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>文本与气泡区域对齐。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化视频洗刷工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1)。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

设置一个混合媒体查看器，该查看器包含一个自定义轨道颜色的视频清理器，高度为10像素，位置从控制栏的上边缘和左边缘起分别为10像素和35像素。

```
.s7mixedmediaviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7mixedmediaviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```
