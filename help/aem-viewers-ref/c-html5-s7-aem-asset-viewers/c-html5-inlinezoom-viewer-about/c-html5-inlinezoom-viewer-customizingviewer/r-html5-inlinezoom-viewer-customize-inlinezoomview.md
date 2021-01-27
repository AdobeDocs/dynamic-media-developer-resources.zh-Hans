---
description: 主视图包括静态图像、在静态图像顶部的弹出视图中显示的缩放图像以及在静态图像顶部显示的提示消息。
seo-description: 主视图包括静态图像、在静态图像顶部的弹出视图中显示的缩放图像以及在静态图像顶部显示的提示消息。
seo-title: 弹出缩放视图
solution: Experience Manager
title: 弹出缩放视图
topic: Dynamic Media
uuid: a918c775-a36a-44e8-9ca4-90cb8f5c3a5e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 3%

---


# 弹出缩放视图{#flyout-zoom-view}

主视图包括静态图像、在静态图像顶部的弹出视图中显示的缩放图像以及在静态图像顶部显示的提示消息。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p> 主视图的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——使主视图透明：

```
.s7flyoutviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

**提示消息的CSS属性**

提示消息的外观由以下CSS类选择器控制：

```
.s7flyoutviewer .s7flyoutzoomview .s7tip
```

可以通过CSS配置字体样式、大小外观和垂直偏移。 但是，水平对齐由查看器逻辑管理。 不支持使用`left`或`right`属性通过CSS覆盖它。

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
   <td colname="col2"> <p>文本颜色. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p>消息文本的边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景填充颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p>消息文本的背景不透明度。 </p> <p>对于Internet Explorer 8，请使用<span class="codeph">滤镜：alpha(opacity-...))</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

提示消息可以本地化。 有关详细信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-localization.md#concept-6c8e58c611934e93ae3f211f46e15c27)。

。

示例——要设置半透明提示消息，其中带有白色的Arial 12px字体，距主视图底部50像素偏移，填充和圆边：

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

