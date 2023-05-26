---
title: 弹出缩放视图
description: 主视图由静态图像和弹出视图中显示的缩放图像组成。 此外，它还包括显示在静态图像上的高亮导航区域，以及显示在静态图像顶部的提示消息。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: c04c4b8f-4e63-4e84-98c0-aa0781608130
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 2%

---

# 弹出缩放视图{#flyout-zoom-view}

主视图由静态图像和弹出视图中显示的缩放图像组成。 此外，它还包括显示在静态图像上的高亮导航区域，以及显示在静态图像顶部的提示消息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

如果正在查看的图像的尺寸与弹出缩放视图的尺寸不匹配，则图像内容将居中在弹出缩放视图的矩形显示区域中。

**主视图的CSS属性**

主视图的外观由以下CSS类选择器控制：

```
.s7flyoutviewer .s7flyoutzoomview
```

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 使主视图透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**弹出视图的CSS属性**

弹出视图的外观由以下CSS类选择器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom
```

<table id="table_85446C72FD914594B7D108381BBFC673"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左侧 </span> </p> </td> 
   <td colname="col2"> <p> 弹出视图相对于主视图左上角的水平位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 顶端 </span> </p> </td> 
   <td colname="col2"> <p> 弹出视图相对于主视图左上角的垂直位置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> 弹出视图的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>弹出视图的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>弹出视图的边框。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 将弹出视图设置为600 x 400像素，在上一个示例中显示的512 x 288主视图的右侧偏移100像素：

```
.s7flyoutviewer .s7flyoutzoomview .s7flyoutzoom { 
 left: 612px; 
 top: 0px; 
 width: 600px; 
 height: 400px;  
}
```

**主视图中高亮显示的CSS属性**

高亮在主视图中的外观由以下CSS类选择器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight
```

可以使用CSS控制背景、边框、透明度和类似属性。 但是，高亮DOM元素的大小和位置由查看器逻辑管理。 不支持通过CSS覆盖它。

<table id="table_F957367566C542829E2F6D296F9DAAC5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> 高亮显示的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p> 突出显示不透明度。 </p> <p>对于Internet Explorer 8，使用 <span class="codeph"> 滤镜：alpha（不透明度 — ...） )； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边界 </span> </p> </td> 
   <td colname="col2"> <p>边框高亮显示。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 要设置透明度为40%的绿色高亮和一个像素红色边框，请执行以下操作：

```
.s7flyoutviewer .s7flyoutzoomview .s7highlight { 
 background-color: green; 
 opacity: 0.4;  
 filter: alpha(opacity = 40); 
 border: 1px solid red; 
}
```

**游标的CSS属性**

时间 `highlightmode` 参数设置为 `cursor`，主视图中的高亮显示被替换为固定大小的光标图稿，它由CSS类选择器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7cursor
```

可以使用CSS控制背景图像和大小。

适用的CSS属性包括：

<table id="table_A86F1E4DE9E84E11AF47373ADC63A459"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image </span> </p> </td> 
   <td colname="col2"> <p>光标图稿。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>光标宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>光标高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>光标支持 `input` 属性选择器，可用于为不同的设备应用不同的光标图稿和大小。 特别是， `input="mouse"` 与桌面系统和 `input="touch"` 对应于触摸设备。

**叠加的CSS属性**

当 `overlay` 参数设置为 `1`，高亮框架或光标图像周围的区域由CSS类选择器控制：

```
 .s7flyoutviewer .s7flyoutzoomview 
.s7overlay
```

<table id="table_A50CA8213C3A4682A081D3D30089574C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>叠加颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>叠加不透明度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**提示消息的CSS属性**

使用以下CSS类选择器控制提示消息的外观：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

可以通过CSS配置字体样式、大小、外观和垂直偏移。 但是，水平对齐是由查看器逻辑管理的。 使用以下方式通过CSS覆盖 `left` 或 `right` 不支持属性。

<table id="table_DCF6B69A9D8C4DB7A10C4572F7484799"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p>从主视图底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-size </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>在消息文本周围填充。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景填充颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景不透明度。 </p> <p>对于Internet Explorer 8，使用 <span class="codeph"> 滤镜：alpha（不透明度 — ...） ) </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

可对提示消息进行本地化。 参见 [用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27) 了解更多信息。

示例 — 要设置半透明提示消息，其中使用白色Arial® 12-px字体、距主视图底部50像素的偏移量、内边距和圆边框：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip { 
bottom: 50px; 
color: #ffffff; 
font-family: Arial; 
font-size: 12px; 
padding-bottom: 10px; 
padding-top: 10px; 
padding-left: 12px; 
padding-right: 12px; 
background-color: #000000; 
border-radius: 4px; 
opacity: 0.5; 
filter: alpha(opacity = 50); 
}
```
