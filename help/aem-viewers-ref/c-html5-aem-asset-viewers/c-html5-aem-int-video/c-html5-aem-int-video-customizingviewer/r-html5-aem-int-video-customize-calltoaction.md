---
title: 行动动员
description: 视频结束时，会显示行动号召面板，并显示与特定视频关联的所有交互式色板。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 43e0ffb3-d650-4b79-ab48-2f32b313b832
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '1299'
ht-degree: 1%

---

# 行动动员{#call-to-action}

视频结束时，会显示行动号召面板，并显示与特定视频关联的所有交互式色板。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

该面板由显示视频标题的标题区域、右上角的重播按钮以及显示为可滚动网格的实际交互式样本组成。 您可以使用[callToActionRecap](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/r-html5-aem-int-video-config-attrib/r-html5-aem-int-video-config-attrib-calltoactionrecap.md#reference-3720b68800684ddabf523e9d81644ce6)配置属性禁用面板。

行动号召面板始终采用整个可用查看器区域。

<!--<a id="section_3A619BE925C04AFA87A6B7846C5C7E2B"></a>-->

以下CSS类选择器控制行动号召面板中背景颜色的外观：

```
.s7interactivevideoviewer .s7calltoaction
```

## 行动号召面板的背景颜色的CSS属性 {#css-properties-of-the-background-color-of-the-call-to-action-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p> 行动号召面板的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example}

要设置具有深灰色背景的行动号召面板，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction { 
    background-color: #222222; 
}
```

<!--<a id="section_AD18C770788B49989BEDAA608ECA804C"></a>-->

以下CSS类选择器控制行动号召面板中标头的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7header
```

## 行动号召面板标题的CSS属性 {#css-properties-of-the-call-to-action-panel-header}

<table id="table_DAA1770AB3074845B5E1B700CD6FC18A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>标题的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>页眉的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下边框</span> </p> </td> 
   <td colname="col2"> <p>页眉的下边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-1}

要设置一个高度为70像素的标题，该标题具有深灰色背景，底部有两个像素边框略浅灰色：

```
.s7interactivevideoviewer .s7calltoaction .s7header { 
    height: 70px; 
    border-bottom: 2px solid #444444; 
    background-color: #222222; 
}
```

<!--<a id="section_B0333FC1A2CC4E089C68D34B839E5156"></a>-->

以下CSS类选择器控制行动号召面板中标题标题的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7header .s7title
```

## 行动号召面板中标题标题的CSS属性：  {#css-properties-of-the-header-title-in-the-call-to-action-panel}

<table id="table_A5E36A5C4C664346B6DAE9A02B36C3D2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p> 横幅中的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p>行高。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p> 字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>横幅中文本的对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左内边距</span> </p> </td> 
   <td colname="col2"> <p>左侧填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充右侧</span> </p> </td> 
   <td colname="col2"> <p> 右内边距，为“重放”按钮留出空间。 </p> </td> 
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

以下CSS类选择器控制“行动号召”面板中关闭按钮的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7closebutton
```

## 行动号召面板中关闭按钮的CSS属性： {#css-properties-of-the-close-button-in-the-call-to-action-panel}

<table id="table_CB0BCBE70DB447BC8D31034A96308924"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>标题顶部的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p>标题右侧的位置，包括内边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>按钮宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> 按钮高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS拼写，则位于图稿拼写内。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，可用于将不同的外观应用于不同的按钮状态。

## 示例 {#example-3}

设置28 x 28像素的重播按钮。 按钮的位置必须从页眉的顶部和右边缘开始20像素。 而且，它必须为四种不同的按钮状态分别显示不同的图像；从组件的Sprite图像中提取图稿：

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

以下CSS类选择器控制“行动号召”面板中缩略图网格视图的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview
```

## 行动号召面板中缩略图网格视图的CSS属性：  {#css-properties-of-the-thumbnail-grid-view-in-the-call-to-action-panel}

<table id="table_A0DDD21C84944D48A639F51FCC8DF065"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>缩略图区域的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-4}

要设置具有深灰色背景的缩略图区域：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview { 
    background-color: #222222; 
}
```

<!--<a id="section_D2E5AADFCE0345468DC0D2977E2765D2"></a>-->

以下CSS类选择器控制行动号召面板中缩略图单元格的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbcell
```

## 行动号召面板中缩略图单元格的CSS属性： {#css-properties-of-the-thumbcell-in-the-call-to-action-panel}

<table id="table_9CEBEF6FC7024F02840A581AEEF612B4"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边距</span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围的水平和垂直边距的大小。 </p> <p>实际水平缩略图间距等于为<span class="codeph"> .s7缩略图</span>设置的左右边距总和。 同样的规则也适用于垂直间距。 </p> </td> 
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

以下CSS类选择器控制行动号召面板中缩略图的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb
```

## 行动号召面板中缩略图的CSS属性： {#css-properties-of-the-thumbnail-in-the-call-to-action-panel}

<table id="table_ECD7477F4BE94BA8943210FA8B6B8D01"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>缩略图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框</span> </p> </td> 
   <td colname="col2"> <p>缩略图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于当前所选图像的缩略图；`state="default"`对应于其余缩略图；`state="over"`用于鼠标悬停操作。

## 示例 {#example-6}

要设置94 x 100像素的缩略图，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumb { 
 width:94px; 
 height:100px; 
}
```

<!--<a id="section_F1B7E3FA3ABD4D71848586A3B308F9E2"></a>-->

以下CSS类选择器控制“行动号召”面板中缩略图标签的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7label
```

## 行动号召面板中缩略图标签的CSS属性： {#css-properties-of-the-thumbnail-label-in-the-call-to-action-panel}

<table id="table_E2C9F21EBD9140FD9D20A4BBAD117E2F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p> 标签的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">文本对齐</span> </p> </td> 
   <td colname="col2"> <p>标签水平对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-7}

要设置使用白色的标签，请居中对齐15像素，然后使用Arial®字体：

```
.s7interactivevideoviewer .s7calltoaction .s7label { 
 text-align: center; 
 color: #ffffff; 
  font-family: Arial,Helvetica,sans-serif; 
  font-size: 15px; 
}
```

<!--<a id="section_2C011101EB804513B942EFB4CBD38E62"></a>-->

如果缩略图多于垂直放入视图的数量，则缩略图会在右侧呈现垂直滚动条。 默认情况下，“行动号召”面板呈现一个没有拇指和滚动按钮的小垂直条。 但是，可以通过更改查看器CSS来自定义栏。

以下CSS类选择器控制“行动号召”面板中滚动条区域的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar
```

## 行动号召面板中滚动条区域的CSS属性： {#css-properties-of-the-scroll-bar-area-in-the-call-to-action-panel}

<table id="table_6D3A4A68BFDB44259A6E2E632B9195F3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 滚动条的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">前</span> </p> </td> 
   <td colname="col2"> <p>垂直滚动条从缩略图区域顶部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">后</span> </p> </td> 
   <td colname="col2"> <p>垂直滚动条从缩略图区域底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右</span> </p> </td> 
   <td colname="col2"> <p> 水平滚动条从缩略图区域的右边缘偏移。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#example-8}

要设置一个宽度为22像素的滚动条，并且该滚动条在缩略图区域的顶部、右侧或底部没有任何边距，请执行以下操作：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar { 
 top:0px; 
 bottom:0px; 
 right:0px; 
 width:22px; 
}
```

<!--<a id="section_E27B7253441543278E1081D70BA46122"></a>-->

滚动条轨道是上下滚动条按钮之间的区域。 组件会自动设置轨道的位置和高度。

以下CSS类选择器控制“行动号召”面板中滚动条轨道的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrolltrack
```

## 滚动轨道条的CSS属性 {#css-properties-of-the-scroll-track-bar}

<table id="table_7A7D40C332F4461FAAC623196C00D5A8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>滚动条宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>轨道栏的背景颜色。 </p> </td> 
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

滚动条缩略图在滚动轨道区域内垂直移动。 其垂直位置完全由组件逻辑控制；但是，缩略图高度不会根据内容量动态变化。

以下CSS类选择器控制缩略图高度和其他方面的外观：

```
.s7interactivevideoviewer .s7calltoaction .s7thumbnailgridview .s7scrollbar .s7scrollthumb
```

## 行动号召面板中缩略图高度的CSS属性： {#css-properties-of-the-thumb-height-in-the-call-to-action-panel}

<table id="table_1F39948FC3924FA4B7F851B65B2D860B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>缩略图宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>缩略图高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充顶端</span> </p> </td> 
   <td colname="col2"> <p>轨道顶部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">填充底部</span> </p> </td> 
   <td colname="col2"> <p>轨道底部之间的垂直边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p>边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>缩略图的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p> 为给定的缩略图状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>缩略图支持`state`属性选择器，该选择器可用于将不同的外观应用于以下不同的缩略图状态： `"up"`、`"down"`、`"over"`和`"disabled"`。

## 示例 {#example-10}

要设置一个像素为6 x 167的滚动条缩略图，它具有三个像素圆角，颜色为灰色，请执行以下操作：

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

无法使用CSS top、left、bottom或right属性定位滚动按钮；查看器逻辑会自动定位它们。 交互式视频查看器中的“行动号召”面板不使用滚动条中的这些按钮，因此其大小在默认CSS中设置为0像素。

## 行动号召面板中顶部和底部滚动按钮的CSS属性：  {#css-properties-of-the-top-and-bottom-scroll-buttons-in-the-call-to-action-panel}

<table id="table_FE17D19E0545424EADB0256524361359"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p> 按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景图像</span> </p> </td> 
   <td colname="col2"> <p>针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景位置</span> </p> </td> 
   <td colname="col2"> <p> 如果使用CSS sprite，则定位在图稿sprite中。 </p> <p>请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>这些按钮支持`state`属性选择器，可用于将不同的外观应用于以下不同的缩略图状态： `"up"`、`"down"`、`"over"`和`"disabled"`。

可以本地化按钮工具提示。 请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74)。

## 示例 {#example-11}

通过将滚动按钮的大小设置为0并隐藏它们来禁用滚动按钮：

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
