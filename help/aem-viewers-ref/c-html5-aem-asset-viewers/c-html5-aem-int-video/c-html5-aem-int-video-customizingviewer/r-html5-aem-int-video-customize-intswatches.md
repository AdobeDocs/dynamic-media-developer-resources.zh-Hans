---
title: 交互式样本
description: 如果在配置中将交互式数据传递给查看器，则交互式样本面板将显示在视频内容旁边。 它由顶部的横幅组成，该横幅可渲染“单击查看”等文本、包含一个或多个交互式样本的列以及两个滚动按钮（仅在桌面系统上可用）。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: c9ef02eb-f5db-474b-b234-c49508e2af35
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '884'
ht-degree: 2%

---

# 交互式样本{#interactive-swatches}

如果在配置中将交互式数据传递给查看器，则交互式样本面板将显示在视频内容旁边。 它由顶部的横幅组成，该横幅可渲染“单击查看”等文本、包含一个或多个交互式样本的列以及两个滚动按钮（仅在桌面系统上可用）。

<!--<a id="section_235621A1533A49AAADB64A7C3191F735"></a>-->

在桌面系统和触控设备上，交互样本将以横向方式垂直渲染到视频内容的右侧。 在纵向的触控设备上，它们以水平一排样本的形式显示在查看器底部。

以下CSS类选择器控制交互式样本面板的位置和方向：

```
.s7interactivevideoviewer .s7interactiveswatches
```

## 交互式样本的CSS属性 {#css-properties-of-the-interactive-swatches}

<table id="table_352DAD495AE742E39B4F12629C43F712"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的宽度 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的顶部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的底部位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的左侧位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 右 </span> </p> </td> 
   <td colname="col2"> <p>交互式样本面板的右位置。 </p> </td> 
  </tr> 
 </tbody> 
</table>

交互式样本面板的运行时位置和方向由上述CSS属性的组合定义，如下所示：

* 要在查看器底部水平渲染交互式样本，请将高度设置为绝对像素值；将左和底部设置为0像素；将宽度、右侧和顶部设置为自动。
* 要垂直渲染交互式样本到视频内容的右侧，请将宽度设置为绝对像素；将右和上设置为0像素；将高度设置为左和下设置为auto。

可以将CSS标记与此样式一起使用，以实现交互式样本面板的自适应放置。

## 示例 {#example}

要设置交互式样本面板，以便在横向的触控设备上在查看器底部水平渲染。 此外，在所有其他情况下，要垂直显示在视频内容的右侧，请执行以下操作：

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

横幅的大小和位置由交互式样本组件根据使用CSS应用的其他样式进行管理，并且无法显式设置。

以下CSS类选择器控制横幅面板的外观：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner
```

## 横幅面板的CSS属性 {#css-properties-of-the-banner-panel}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>横幅面板的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>横幅面板中的文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>横幅面板周围的边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-weight </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体粗细。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板中文本的字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-align </span> </p> </td> 
   <td colname="col2"> <p>用于横幅面板内文本的字体对齐方式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以本地化横幅工具提示。 参见 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 了解更多信息。

## 示例 {#section-e8caea0a303c425a8a637c2a47c06355}

要设置具有深灰色背景、浅灰色双像素边框和白色文本水平居中的横幅，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7banner { 
    background-color: #222222; 
    border-bottom: 2px solid #444444; 
    color: #ffffff; 
    text-align: center; 
}
```

以下CSS类选择器控制样本的外观：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches
```

## 样本区域的CSS属性 {#css-properties-of-the-swatches-area}

<table id="table_45E98E96B07246CAA5D3076FAF62A0B3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>样本区域的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-9cadd62a09fd44a280f55ff42437e416}

要设置具有深灰色背景的样本区域，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches { 
    background-color: #222222; 
}
```

以下CSS类选择器控制样本缩略图之间的间距：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell`

## 样本缩略图间距的CSS属性 {#css-properties-of-the-swatches-thumbnail-spacing}

<table id="table_FE6A749EA3894956998D50EA4AB6497B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin </span> </p> </td> 
   <td colname="col2"> <p> 每个缩略图周围的水平和垂直边距的大小。 实际缩略图间距等于为设置的左右边距之和 <span class="codeph"> .s7thumbcell </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-39fb270b7e494a9d99e6e8f6890ec53c}

要将垂直间距设置为十像素，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumbcell { 
 margin: 5px; 
}
```

以下CSS类选择器控制各个缩略图的外观：

`.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7thumb`

## 单个缩略图外观的CSS属性 {#css-properties-of-the-appearance-of-individual-thumbnails}

<table id="table_FB760FE6BEA44E129C07DD912C86DE57"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>缩略图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
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
>缩略图支持 `state` 属性选择器，可用于将不同的外观应用于不同的缩略图状态。 特别是， `state="selected"` 对应于当前选定图像的缩略图； `state="default"` 与其余缩略图相对应； `state="over"` 用于鼠标悬停。

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
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>标签边框。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> text-align </span> </p> </td> 
   <td colname="col2"> <p>水平文本对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-eb141eb6c1154183baa69796edb90536}

要设置标签以使用左对齐、白色、12像素、Helvetica®字体和下边框，请执行以下操作：

```
.s7interactivevideoviewer .s7interactiveswatches .s7swatches .s7label { 
 border-bottom: 1px solid #e9e9e9; 
 text-align: left; 
color: #ffffff; 
font-family: Helvetica,sans-serif; 
font-size: 12px; 
}
```

以下CSS类选择器控制向上和向下滚动按钮的外观：

`.s7interactivevideoviewer .s7interactiveswatches .s7scrollupbutton`

`.s7interactivevideoviewer .s7interactiveswatches .s7scrolldownbutton`

无法使用CSS定位滚动按钮 `top`， `left`， `bottom`、和 `right` 属性；相反，查看器逻辑会自动定位它们。

## 上下滚动按钮外观的CSS属性 {#css-properties-of-the-appearance-of-the-up-and-down-scroll-buttons}

<table id="table_48AF27AFBB1543288D45449D6900675C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>滚动按钮的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>针对给定按钮状态显示的图像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position </span> </p> </td> 
   <td colname="col2"> <p>如果使用CSS sprite，则为图稿sprite内的位置。 </p> <p>另请参阅 <a href="../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#section-9b6d8d601cb441d08214dada7bb4eddc" format="dita" scope="local"> CSS脚本 </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>此按钮支持 `state` 属性选择器，可用于将不同的外观应用于按钮状态：&#39;&#39; `up`“， ” `down`“， ” `over`“”和“” `disabled`“。

可对按钮工具提示进行本地化。 参见 [用户界面元素的本地化](../../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74) 了解更多信息。

## 示例 {#section-e6ce4fa084b84288bc7583342b2c510c}

要设置一个60 x 36像素的向上滚动按钮，请为每个状态使用不同的图稿，并从组件的sprite图像中获得该图稿：

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
