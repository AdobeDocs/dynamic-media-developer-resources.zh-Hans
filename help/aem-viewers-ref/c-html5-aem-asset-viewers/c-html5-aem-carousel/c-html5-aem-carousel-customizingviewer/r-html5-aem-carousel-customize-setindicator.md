---
description: “设置指示符”是在查看器底部渲染的一系列点。 它显示集内的当前位置。
solution: Experience Manager
title: 设置指示符
feature: Dynamic Media Classic，查看器，SDK/API，传送横幅
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 1%

---


# 设置指示符{#set-indicator}

“设置指示符”是在查看器底部渲染的一系列点。 它显示集内的当前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示符的CSS属性**

使用以下CSS类选择器控制设置指示符容器的外观：

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>设置指示符的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符支持模式属性选择器，您可以使用它对点线和数字操作模式应用不同的样式。 具体而言，`mode="numeric"`对应于数字操作模式；`mode="dotted"`对应于默认点状态。

示例 — 设置白色背景的设置指示符：

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
   <td colname="col1"> <p> <span class="codeph"> 边距左  </span> </p> </td> 
   <td colname="col2"> <p>左边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 上边距  </span> </p> </td> 
   <td colname="col2"> <p>上边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距右  </span> </p> </td> 
   <td colname="col2"> <p>右边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距 — 底部  </span> </p> </td> 
   <td colname="col2"> <p>底边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius  </span> </p> </td> 
   <td colname="col2"> <p>边框半径（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>十六进制格式的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> font-family  </span> </p> </td> 
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
>设置指示符项支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是`state="selected"`对应于集合中的当前元素；`state="unselected"`对应于默认项目状态。

示例 — 在虚线模式下设置指示符，以使桌面系统距查看器底部20像素。 未选中的点为黑色，透明度为50%,15 x 15像素，圆角为7像素。 所选点为黑色，透明度为90%,18 x 18像素，圆角为9像素。 点之间的间距为5像素。

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

