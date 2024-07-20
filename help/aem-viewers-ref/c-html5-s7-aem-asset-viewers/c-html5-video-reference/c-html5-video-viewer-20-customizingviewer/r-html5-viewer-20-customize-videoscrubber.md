---
title: 视频洗刷
description: 视频洗刷是水平滑块控件，允许用户动态搜索到当前播放视频内的任何时间位置
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 404e39d4-565e-4dde-b2bd-fa83a895d001
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 0%

---

# 视频洗刷{#video-scrubber}

视频洗刷是水平滑块控件，允许用户动态搜索到当前播放视频内的任何时间位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

清理器“旋钮”也会在视频播放时移动，以指示视频在播放期间的当前时间位置。 视频清理器始终占据控制栏的全部宽度。 可以通过CSS为视频洗刷蒙皮并更改其高度和垂直位置。

视频清理器的常规外观由以下CSS类选择器控制：

```
.s7videoviewer .s7videoscrubber 
.s7videoviewer .s7videoscrubber .s7videotime 
.s7videoviewer .s7videoscrubber .s7knob
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
.s7videoviewer .s7videoscrubber .s7track 
.s7videoviewer .s7videoscrubber .s7trackloaded 
.s7videoviewer .s7videoscrubber .s7trackplayed
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
.s7videoviewer .s7videoscrubber .s7knob
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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

以下CSS类选择器控制播放时间气泡：

```
.s7videoviewer .s7videoscrubber .s7videotime
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
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>文本与气泡区域对齐。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化视频洗刷工具提示。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-localization.md#concept-1d5ca2d8480f4064a51eddba13940aad)。

**示例** — 为视频查看器设置带有自定义轨道颜色的视频清理器。 清理器必须高10个像素，并且位于控制栏上边缘和左边缘的10个像素和35个像素的位置。

```
.s7videoviewer .s7videoscrubber  { 
top:10px; 
left:35px; 
height:10px; 
background-color:#AAAAAA; 
} 
.s7videoviewer .s7videoscrubber .s7track { 
height:10px; 
background-color:#444444; 
} 
.s7videoviewer .s7videoscrubber .s7trackloaded { 
height:10px; 
background-color:#666666; 
} 
.s7videoviewer .s7videoscrubber .s7trackplayed { 
height:10px; 
background-color:#888888; 
}
```

使用`navigation`参数启用视频章节设置时，章节位置将作为标记显示在视频洗刷跟踪的顶部。

视频章节标记由以下CSS类选择器控制：

```
 .s7videoviewer .s7videoscrubber .s7navigation
```

视频章节标记的&#x200B;**CSS属性**

<table id="table_51F16E47BEF3430B919ABEEDBE543973"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>视频章节标记宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>视频章节标记高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>视频章节标记图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮同时支持`state`属性选择器，您可以使用它来将不同的外观应用于不同的按钮状态。 特别是，`selected='default'`对应于默认的视频章节标记状态，当鼠标悬停在手势或触摸手势上激活视频章节标记时，将使用`selected='over'`。

**示例** — 设置一个5 x 8像素的视频章节标记，该标记在“默认”和“超过”状态使用不同的艺术品。

```
.s7videoviewer .s7videoscrubber .s7navigation { 
width:5px; 
height:8px; 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="default"] { 
background-image: url("images/v2/VideoScrubberDiamond.png"); 
} 
.s7videoviewer .s7videoscrubber .s7navigation[state="over"] { 
background-image: url("images/v2/VideoScrubberDiamond_over.png"); 
}
```

视频章节气泡位于视频章节标记器的顶部，可显示给定章节的标题、开始时间和描述。 可以控制相对于视频洗刷轨道的最大气泡宽度和垂直偏移。 其余由组件自动计算。

视频章节气泡由以下CSS类选择器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter
```

视频章节泡的&#x200B;**CSS属性**

<table id="table_7F33738422F84978B9132495F67C2156"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">最大宽度</span> </p> </td> 
   <td colname="col2"> <p>视频章节气泡的最大宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>与视频洗刷轨道的垂直偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 设置宽为235像素且从视频洗刷轨道底部向上八像素的视频章节气泡。

```
.s7videoviewer .s7videoscrubber .s7chapter { 
max-width:235px; 
bottom:8px; 
}
```

视频章节气泡包含可选标题和内容。 标题具有可选的章节开始时间和章节标题。

标头由以下CSS类选择器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header
```

视频章节气泡标题的&#x200B;**CSS属性**

<table id="table_56FBC3BADDEA4E15924DD750CADC474F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>视频章节气泡标题高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>视频章节气泡标题文本的内部边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>视频章节气泡标题背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p>视频章节气泡标题文本行高。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 设置高22像素、行高22像素、水平边距12像素和灰色背景的视频章节气泡标题。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header { 
height:22px; 
padding:0 12px; 
line-height:22px; 
background-color: rgba(51, 51, 51, 0.8); 
}
```

视频章节的开始时间由以下CSS类选择器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime
```

视频章节开始时间的&#x200B;**CSS属性**

<table id="table_D58D6B22BAEE4E26BAAB34783AE5A044"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充右侧</span> </p> </td> 
   <td colname="col2"> <p> 开始时间和章节标题之间的边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 若要设置章节开始时间，请使用灰色10像素Verdana字体并在右侧填充10像素。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7starttime { 
color: #dddddd; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
padding-right: 10px; 
}
```

视频章节标题由以下CSS类选择器控制：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title
```

视频章节标题的&#x200B;**CSS属性**

<table id="table_240DD3E119584DCC95FF480B60266603"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>视频章节标题文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>视频章节标题字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>视频章节标题字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>视频章节标题字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 设置使用白色、粗体、10像素Verdana字体的视频章节标题。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7header .s7title { 
color: #ffffff; 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 10px; 
font-weight: bold; 
}
```

视频章节描述由以下CSS类选择器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7description
```

视频章节描述的&#x200B;**CSS属性**

<table id="table_780382ECB3D049118857DCA21D130326"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体粗细</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充</span> </p> </td> 
   <td colname="col2"> <p>视频章节描述内边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 若要设置视频章节描述，请使用深灰色、11像素的Verdana字体，背景为浅灰色。 最后，采用5像素行高、12像素水平边距、12像素上边距、9像素下边距。

```
.s7videoviewer .s7videoscrubber .s7chapter .s7description { 
color: #333333; 
background-color: rgba(221, 221, 221, 0.9); 
font-family: Verdana,Arial,Helvetica,sans-serif; 
font-size: 11px; 
line-height: 15px; 
padding: 12px 12px 9px; 
}
```

章节气泡底部的楔形连接器由以下CSS类选择器控制：

```
 .s7videoviewer .s7videoscrubber .s7chapter .s7tail
```

楔形连接器的&#x200B;**CSS属性**

<table id="table_BC6AFB57D9404A84A3AE657448C0EB06"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框颜色</span> </p> </td> 
   <td colname="col2"> <p>楔形连接器的颜色。 </p> <p>定义为<span class="codeph"> &lt;color&gt;透明</span>，以便只定义顶部边框颜色，其余边框保持透明。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框宽度</span> </p> </td> 
   <td colname="col2"> <p> 楔形连接器宽度。 </p> <p>定义为<span class="codeph"> &lt;width&gt; &lt;width&gt; 0 </span>，以便仅为顶边框和水平边框定义相同的宽度，而底边框宽度为<span class="codeph"> 0 </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p> 仅定义负下边距。 它应具有与<span class="codeph">边框宽度</span>相同的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**示例** — 要设置灰色、6像素楔形连接器：

```
.s7videoviewer .s7videoscrubber .s7chapter .s7tail { 
border-color: rgba(221, 221, 221, 0.9) transparent transparent; 
border-width: 6px 6px 0; 
margin: 0 0 0 -6px; 
}
```
