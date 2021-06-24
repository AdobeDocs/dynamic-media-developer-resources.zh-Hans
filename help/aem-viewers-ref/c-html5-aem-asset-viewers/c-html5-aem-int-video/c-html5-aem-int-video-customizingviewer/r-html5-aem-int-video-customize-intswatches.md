---
description: 如果在配置中将交互式数据传递到查看器，则交互式样本面板会显示在视频内容旁边。 它由顶部的一个横幅组成，该横幅可呈现文本，如“点击查看”、一个或多个交互式色板的列以及两个滚动按钮（仅在桌面系统上可用）。
solution: Experience Manager
title: 交互式色板
feature: Dynamic Media Classic，查看器，SDK/API，交互式视频
role: Developer,Business Practitioner
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '892'
ht-degree: 2%

---

# 交互式色板{#interactive-swatches}

如果在配置中将交互式数据传递到查看器，则交互式样本面板会显示在视频内容旁边。 它由顶部的一个横幅组成，该横幅可呈现文本，如“点击查看”、一个或多个交互式色板的列以及两个滚动按钮（仅在桌面系统上可用）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

在桌面系统和触控设备上，交互式色板以横向方向垂直呈现在视频内容的右侧。 在以纵向方向显示的触控设备上，这些设备以水平行的色板形式显示在查看器底部。

以下CSS类选择器控制交互式色板面板的位置和方向：

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 交互式色板的CSS属性 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的宽度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的顶部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的底部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的左侧位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>交互式色板面板的右侧位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

交互式色板面板的运行时位置和方向由上述CSS属性的组合定义，如下所示：

* 要在查看器底部水平渲染交互式色板，请将高度设置为绝对像素值；左和下到0px;宽度、右侧和从上到上的自动。
* 要在视频内容的右侧垂直渲染交互式色板，请将宽度设置为绝对像素；右上至0px;高度，从左到下到自动。

可以将CSS标记与此样式结合使用，以实现交互式色板面板的自适应放置。

## 示例 {#example}

要设置一个交互式色板面板，以便在触控设备上在查看器底部以横向水平呈现，并在所有其他情况下以垂直方式显示视频内容的右侧：

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7interactiveswatches, 
.s7interactivevideoviewer.s7mouseinput .s7interactiveswatches { 
 width:120px; 
 height:auto; 
 right:0px; 
 top:0px; 
 left:auto; 
 bottom:auto; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7interactiveswatches { 
 width:auto; 
 height:136px; 
 right:auto; 
 top:auto; 
 left:0px; 
 bottom:0px; 
}
```

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

横幅的大小和位置由交互式色板组件根据应用于CSS的其他样式来管理，并且无法进行显式设置。

以下CSS类选择器控制横幅面板的外观：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 横幅面板的CSS属性 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>横幅面板的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>横幅面板内的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>横幅面板周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体粗细  </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内的文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align  </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体对齐方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以对横幅工具提示进行本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有深灰色背景、浅灰色两像素边框和水平居中白色文本的横幅，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

以下CSS类选择器控制色板的外观：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## 色板区域的CSS属性 {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>色板区域的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-9cadd62a09fd44a280f55ff42437e416}

要设置具有深灰色背景的色板区域，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

以下CSS类选择器控制色板缩览图之间的间距：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 样本缩略图间距的CSS属性 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围的水平和垂直边距的大小。 实际缩略图间距等于为<span class="codeph"> .s7thumbcell </span>设置的左边距和右边距的和。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

要将垂直间距设置为10像素，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

以下CSS类选择器控制单个缩略图的外观：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 单个缩略图外观的CSS属性 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
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
>缩略图支持`state`属性选择器，您可以使用该选择器将不同的外观应用到不同的缩略图状态。 尤其是`state="selected"`对应于当前选定图像的缩略图；`state="default"`对应其余缩略图；`state="over"`用于鼠标悬停。

## 示例 {#section-69fec189ffaa440b97b6b846c320b75b}

要设置100 x 75像素的缩略图，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb { 
 width:100px; 
 height:75px; 
}
```

以下CSS类选择器控制缩略图标签的外观：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label`

## 缩略图标签外观的CSS属性 {#css-properties-of-the-appearance-of-the-thumbnail-label}

<table id="table_81B3209FB8124FFA9DB81FD35717900D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 颜色  </span> </p> </td> 
   <td colname="col2"> <p>文本颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>标记边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align  </span> </p> </td> 
   <td colname="col2"> <p>水平文本对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-eb141eb6c1154183baa69796edb90536}

要设置标签以使用左对齐、白色、12像素、Helvetica字体和下边框，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

以下CSS类选择器控制上下滚动按钮的外观：

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

无法使用CSS `top`、`left`、`bottom`和`right`属性定位滚动按钮；相反，查看器逻辑会自动定位它们。

## 上下滚动按钮外观的CSS属性 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 宽度  </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 高度  </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景图像  </span> </p> </td> 
   <td colname="col2"> <p>为给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景位置  </span> </p> </td> 
   <td colname="col2"> <p>使用CSS Sprite时图稿Sprite内的位置。 </p> <p>另请参阅<a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS Sprite </a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持`state`属性选择器，您可以使用该选择器对按钮状态应用不同的外观：&quot; `up`&quot;、&quot; `down`&quot;、&quot; `over`&quot;和&quot; `disabled`&quot;。

可以对按钮工具提示进行本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 。

## 示例 {#section-e6ce4fa084b84288bc7583342b2c510c}

要设置60 x 36像素的向上滚动按钮，请为每个状态提供不同的图稿，并从组件的Sprite图像中获取该图稿：

```
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton { 
 background-size: 120px; 
 width: 60px; 
 height: 36px;  
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state] { 
 background-image: url(images/v2/InteractiveSwatches_light_sprite.png); 
} 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='up'] { background-position: -60px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='over'] { background-position: -0px -684px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='down'] { background-position: -60px -648px; } 
.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton[state='disabled'] { background-position: -0px -648px; }
```
