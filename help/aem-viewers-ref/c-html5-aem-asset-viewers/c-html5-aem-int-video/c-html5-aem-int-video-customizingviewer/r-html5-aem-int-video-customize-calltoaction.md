---
description: 视频结束时，“行动动员”面板会显示，并显示与特定视频关联的所有交互式色板。
solution: Experience Manager
title: 行动动员
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1283'
ht-degree: 3%

---

# 行动动员{#call-to-action}

视频结束时，“行动动员”面板会显示，并显示与特定视频关联的所有交互式色板。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

该面板由显示视频标题的标题区域、右上角的重播按钮以及显示为可滚动网格的实际交互式样本组成。 您可以使用[callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6)配置属性禁用该面板。

“行动动员”面板始终包含整个可用的查看器区域。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

以下CSS类选择器控制“行动动员”面板中背景颜色的外观：

```
.s7interactivevideoviewer .s7calltoaction
```

## 行动动员面板背景颜色的CSS属性 {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 行动动员面板的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example}

要设置具有深灰色背景的行动动员面板，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

以下CSS类选择器控制标题在行动动员面板中的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## 操作调用面板标题的CSS属性 {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>标题的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>标题的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-bottom  </span> </p> </td> 
   <td colname="col2"> <p>标题的下边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-1}

要设置高度为70像素的标头，其背景为深灰色，底部的两个像素边框略为浅灰色：

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

以下CSS类选择器控制在行动动员面板中标题的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## 行动动员面板中标题的CSS属性：  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p> 横幅中的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行高  </span> </p> </td> 
   <td colname="col2"> <p>行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p> 字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>横幅中文本的对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左边距  </span> </p> </td> 
   <td colname="col2"> <p>左边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 内边距 — 右边距  </span> </p> </td> 
   <td colname="col2"> <p> 用于为重播按钮留出空间的右边距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-2}

要设置具有70像素行高、25像素字体大小、白色和左对齐的视频标题，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title { 
    line-height: 70px; 
    font-size: 25px; 
    color: #ffffff; 
    text-align: left; 
}
```

<!--<a id="section_D23A6D4BA0614286A060982B359E3C08"></a>-->

以下CSS类选择器控制“行动动员”面板中关闭按钮的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## 行动动员面板中关闭按钮的CSS属性： {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>从标题顶部的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>标题右侧的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p> 按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>在图稿快照集内放置（如果使用CSS快照）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的按钮状态。

## 示例 {#example-3}

设置28 x 28像素的重播按钮；从头顶和右边缘定位20像素；为四个不同的按钮状态中的每一个状态显示不同的图像；从组件的sprite图像中获取图稿：

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton { 
 top: 20px; 
 right: 20px; 
 background-size: 336px; 
 width: 28px; 
 height: 28px;  
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state] { 
 background-image: url(images/v2/PlayPauseButton_sprite.png); 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='up'] { 
 background-position: -28px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='over'] { 
 background-position: -0px -1260px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='down'] { 
 background-position: -28px -1232px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7closebutton[state='disabled'] { 
 background-position: -0px -1232px; 
}
```

<!--<a id="section_3975B58E78DE4E81B469372FB8A3A348"></a>-->

以下CSS类选择器控制在行动动员面板中缩略图网格视图的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## 行动动员面板中缩略图网格视图的CSS属性：  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>缩略图区域的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-4}

要设置具有深灰色背景的缩略图区域，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

以下CSS类选择器控制“行动动员”面板中缩览图单元格的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## 行动动员面板中缩略图的CSS属性： {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围的水平和垂直边距的大小。 </p> <p>实际水平缩略图间距等于为<span class="codeph"> .s7thumbcell </span>设置的左边距和右边距的和。 同样的规则也适用，但适用于垂直间距。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-5}

要设置24像素的水平间距和18像素的垂直间距，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell { 
 margin-top: 9px; 
 margin-bottom: 9px; 
 margin-left: 12px; 
 margin-right: 12px; 
}
```

<!--<a id="section_D06CF9F709A3447F83DC6E1CE7CA58B5"></a>-->

以下CSS类选择器控制在行动动员面板中缩略图的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## 行动动员面板中缩略图的CSS属性： {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>缩略图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>缩略图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的缩略图状态。 特别是，`state="selected"`对应于当前选定图像的缩略图；`state="default"`对应其余缩略图；`state="over"`用于鼠标悬停。

## 示例 {#example-6}

要设置94 x 100像素的缩略图，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

以下CSS类选择器控制在行动动员面板中缩略图标签的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## 行动动员面板中缩略图标签的CSS属性： {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p> 标签的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>标签的水平对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-7}

要设置使用白色的标签，请居中对齐15像素，并使用Arial字体：

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

如果缩览图的缩览图数量超过垂直可查看缩略图数量，则缩览图会在右侧呈现垂直滚动条。 默认情况下，“行动动员”面板会呈现一个没有拇指和滚动按钮的小垂直条。 但是，可以通过更改查看器CSS来自定义栏。

以下CSS类选择器控制操作调用面板中滚动条区域的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## 行动动员面板中滚动条区域的CSS属性： {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p> 滚动条的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>垂直滚动条与缩略图区域顶部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>垂直滚动条与缩览图区域底部的偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p> 缩略图区域右边缘的水平滚动条偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-8}

要设置宽度为22像素的滚动条，并且该滚动条与缩略图区域的顶部、右侧或底部之间没有任何边距：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

滚动条轨道是顶部和底部滚动条按钮之间的区域。 该组件会自动设置轨道的位置和高度。

以下CSS类选择器控制操作调用面板中滚动条轨道的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## 滚动跟踪栏的CSS属性 {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>滚动跟踪栏的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>跟踪栏的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-9}

要设置宽度为22像素且颜色为灰色的滚动条轨道，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack { 
 width:22px; 
 background-color:#222222; 
}
```

<!--<a id="section_4A5D8C1A9C9D4E7B8AC0CD5BC6F3772D"></a>-->

滚动条拇指在滚动轨道区域内垂直移动。 其垂直位置完全由组件逻辑控制；但是，缩览图高度不会根据内容的数量动态更改。

以下CSS类选择器控制缩览图高度和其他方面的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## 行动动员面板中缩览图高度的CSS属性： {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>拇指宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>拇指高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-top  </span> </p> </td> 
   <td colname="col2"> <p>轨道顶部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> padding-bottom  </span> </p> </td> 
   <td colname="col2"> <p>轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框半径  </span> </p> </td> 
   <td colname="col2"> <p>边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>拇指的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p> 为给定的拇指状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩览图支持`state`属性选择器，该选择器可用于对以下不同的缩览图状态应用不同的外观：`"up"`、`"down"`、`"over"`和`"disabled"`。

## 示例 {#example-10}

要设置6 x 167像素、三个像素圆角和灰色的滚动条缩览图，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb[state] { 
 width:6px; 
 height:167px; 
 background-color:#666666; 
 background-image:none; 
 border-radius:3px 3px 3px 3px; 
}
```

<!--<a id="section_C393B59763344E70A3BBD0601110F8DD"></a>-->

以下CSS类选择器控制顶部和底部滚动按钮的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton 
 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton
```

无法使用CSS top、left、bottom或right属性定位滚动按钮；查看器逻辑会自动定位它们。 交互式视频查看器中的“行动动员”面板在滚动条中不使用这些按钮，因此在默认CSS中，它们的大小将设置为0像素。

## “操作调用”面板中顶部和底部滚动按钮的CSS属性：  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p> 按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p> 在图稿Sprite中放置（如果使用CSS Sprite）。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>这些按钮支持`state`属性选择器，该选择器可用于将不同的外观应用于以下不同的拇指状态：`"up"`、`"down"`、`"over"`和`"disabled"`。

可以对按钮工具提示进行本地化。 请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 示例 {#example-11}

通过将滚动按钮的大小设置为0并隐藏按钮，可禁用滚动按钮：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollupbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
} 
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolldownbutton { 
 visibility: hidden; 
 width: 0px; 
 height: 0px; 
}
```
