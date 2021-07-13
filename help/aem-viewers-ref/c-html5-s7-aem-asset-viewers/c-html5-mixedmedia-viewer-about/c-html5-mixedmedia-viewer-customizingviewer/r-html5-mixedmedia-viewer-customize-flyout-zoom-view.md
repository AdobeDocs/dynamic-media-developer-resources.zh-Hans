---
description: 在内联缩放模式下，主视图由静态图像、在弹出视图中显示的缩放图像以及在静态图像顶部显示的提示消息组成。
solution: Experience Manager
title: 弹出缩放视图
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,User
exl-id: 46c91d1f-5809-4270-a06d-5068d20a6341
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 5%

---

# 弹出缩放视图{#flyout-zoom-view}

在内联缩放模式下，主视图由静态图像、在弹出视图中显示的缩放图像以及在静态图像顶部显示的提示消息组成。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**主查看器区域的CSS属性**

主视图的外观通过以下CSS类选择器进行控制：

```
.s7mixedmediaviewer .s7flyoutzoomview
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

示例 — 使主视图透明：

```
.s7mixedmediaviewer .s7flyoutzoomview { 
 background-color: transparent; 
}
```

<!--<a id="section_FD07AB77593748F99DC6C42ED20A61EC"></a>-->

使用以下CSS类选择器控制提示消息的外观：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip
```

可以通过CSS配置字体样式、大小外观和垂直偏移。 但是，水平对齐由查看器逻辑管理。 不支持使用`left`或`right`属性通过CSS覆盖该域。

**提示消息的CSS属性**

<table id="table_5417B0C0343747649502629F43DF231A"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>消息背景填充颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框半径  </span> </p> </td> 
   <td colname="col2"> <p> 消息背景边框半径。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 底部 </span> </p> </td> 
   <td colname="col2"> <p> 从主视图底部偏移。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>提示文本颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体大小. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体系列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 不透明度  </span> </p> </td> 
   <td colname="col2"> <p> 消息背景不透明度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 填充 </span> </p> </td> 
   <td colname="col2"> <p> 在消息文本周围填充。 </p> </td> 
  </tr> 
 </tbody> 
</table>

提示消息可以本地化。 有关更多信息，请参阅[用户界面元素的本地化](../../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-localization.md#concept-16262b8096474d6c9c018c3e99110dd1) 。

示例 — 要设置半透明提示消息，其中Arial字体为12px，距主视图底部50像素偏移，填充以及四舍五入的边框：

```
.s7mixedmediaviewer .s7flyoutzoomview .s7tip { 
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
