---
description: 设置指示器是在查看器底部呈现的一系列点。 它显示集内的当前位置。
solution: Experience Manager
title: 设置指示器
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# 设置指示器{#set-indicator}

设置指示器是在查看器底部呈现的一系列点。 它显示集内的当前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示器的CSS属性**

使用以下CSS类选择器控制设置指示器容器的外观：

```
.s7carouselviewer .s7setindicator
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
   <td colname="col2"> <p>以十六进制格式表示的设置指示器的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示器支持模式属性选择器，您可以使用该选择器对点线和数字操作模式应用不同的样式。 具体而言，`mode="numeric"`对应于数字操作模式；`mode="dotted"`对应于默认的点状态。

示例 — 要设置带白色背景的设置指示器：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示器点的外观由CSS类选择器控制。 它适用于点线和数字操作模式下的项目。

`.s7carouselviewer .s7setindicator .s7dot`

<table id="table_09B6E232FB94417392D101A7A653BE54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS属性 </p> </th> 
   <th colname="col2" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>设置指示器点的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>设置指示器点的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 左  </span> </p> </td> 
   <td colname="col2"> <p>左边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 顶部  </span> </p> </td> 
   <td colname="col2"> <p>上边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距右侧  </span> </p> </td> 
   <td colname="col2"> <p>右边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 底部  </span> </p> </td> 
   <td colname="col2"> <p>下边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边框半径  </span> </p> </td> 
   <td colname="col2"> <p>边框半径（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体大小  </span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字体的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直对齐  </span> </p> </td> 
   <td colname="col2"> <p>横幅索引的垂直对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行高  </span> </p> </td> 
   <td colname="col2"> <p>横幅索引的文本高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示器项支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的缩略图状态。 其中，`state="selected"`对应于集合中的当前元素；`state="unselected"`对应于默认项目状态。

示例 — 在虚线模式下设置指示器，以便桌面系统距查看器底部20像素。 未选择的点是黑色的，其透明度为50%,15 x 15像素，圆角为7像素。 选定的点是黑色的，其透明度为90%,18 x 18像素，圆角为9像素。 点之间的间距为5像素。

```
.s7carouselviewer.s7mouseinput .s7setindicator { 
 bottom: 20px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot{ 
 width:15px; 
 height:15px; 
 margin-left:2.5px; 
 margin-right:2.5px; 
 margin-top:2.5px; 
 margin-bottom:2.5px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='selected'] {  
 width:18px; 
 height:18px; 
 background-color: #000000; 
 opacity: 0.9; 
 border-radius:9px; 
} 
.s7carouselviewer.s7mouseinput .s7setindicator[mode='dotted'] .s7dot[state='unselected'] {  
 width:15px; 
 height:15px; 
 background-color: #000000; 
 opacity: 0.5; 
 border-radius:7px; 
}
```
