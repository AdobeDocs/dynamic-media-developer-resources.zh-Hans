---
description: 设置指示符是在查看器底部渲染的一系列点。 它显示集合中的当前位置。
seo-description: 设置指示符是在查看器底部渲染的一系列点。 它显示集合中的当前位置。
seo-title: 设置指示符
solution: Experience Manager
title: 设置指示符
topic: Dynamic Media
uuid: 3f90a216-654f-44a9-947d-592bd5f342d4
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 设置指示符{#set-indicator}

设置指示符是在查看器底部渲染的一系列点。 它显示集合中的当前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示符的CSS属性**

设置指示符容器的外观由以下CSS类选择器控制：

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
   <td colname="col2"> <p>设置指示符的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符支持模式属性选择器，您可以使用它对点和数字操作模式应用不同的样式。 具体来说，`mode="numeric"`对应于数字操作模式；`mode="dotted"`对应于默认点状态。

示例——设置具有白色背景的设置指示符：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示符点的外观由CSS类选择器控制。 它适用于点线和数字操作模式下的项目。

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
   <td colname="col2"> <p>设置指示符点的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>设置指示符点的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 左边距  </span> </p> </td> 
   <td colname="col2"> <p>左边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上边距  </span> </p> </td> 
   <td colname="col2"> <p>上边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距右侧  </span> </p> </td> 
   <td colname="col2"> <p>右边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距——底部  </span> </p> </td> 
   <td colname="col2"> <p>底边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>边框半径（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色  </span> </p> </td> 
   <td colname="col2"> <p>十六进制格式的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字体系列  </span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 字号  </span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> color </span> </p> </td> 
   <td colname="col2"> <p>字体的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 垂直对齐  </span> </p> </td> 
   <td colname="col2"> <p>横幅索引的垂直对齐。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 行高  </span> </p> </td> 
   <td colname="col2"> <p>横幅索引的文本高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符项支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的缩略图状态。 特别是`state="selected"`对应于集合中的当前元素；`state="unselected"`对应于默认项状态。

示例——在虚线模式下设置指示符，使桌面系统距查看器底部20像素。 未选中的点为黑色，具有50%的透明度，15 x 15像素，7像素为圆角。 选定的点为黑色，透明度为90%,18 x 18像素，圆角为9像素。 点之间的间距为5像素。

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

