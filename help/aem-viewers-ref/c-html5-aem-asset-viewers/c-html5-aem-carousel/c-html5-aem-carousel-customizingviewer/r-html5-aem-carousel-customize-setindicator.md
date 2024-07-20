---
title: 设置指示器
description: 设置指示器是呈现在查看器底部的一系列点。 它显示集合中的当前位置。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 7d0827c5-f420-4804-983c-5298ee92b276
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 0%

---

# 设置指示器{#set-indicator}

设置指示器是呈现在查看器底部的一系列点。 它显示集合中的当前位置。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

设置指示器的&#x200B;**CSS属性**

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>设置指示器的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示器支持模式属性选择器，您可以使用它来为点状和数字操作模式应用不同的样式。 特别是，`mode="numeric"`对应于数值操作模式；`mode="dotted"`对应于默认点状态。

例如，假设您要设置一个具有白色背景的设置指示器：

```
.s7carouselviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示符点的外观由CSS类选择器控制。 它适用于点状和数字运算模式下的项目。

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
   <td colname="col1"> <p> <span class="codeph">宽度</span> </p> </td> 
   <td colname="col2"> <p>设置指示器点的宽度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p>设置指示器点的高度。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">左边距</span> </p> </td> 
   <td colname="col2"> <p>左边距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">上边距</span> </p> </td> 
   <td colname="col2"> <p>上边距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">右边距</span> </p> </td> 
   <td colname="col2"> <p>以像素为单位的右边距。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下边距</span> </p> </td> 
   <td colname="col2"> <p>下边距（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">边框半径</span> </p> </td> 
   <td colname="col2"> <p>边框半径（像素）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>以十六进制格式表示的背景颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体系列</span> </p> </td> 
   <td colname="col2"> <p>字体名称。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">字体大小</span> </p> </td> 
   <td colname="col2"> <p>字体大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">颜色</span> </p> </td> 
   <td colname="col2"> <p>字体的颜色。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">垂直对齐</span> </p> </td> 
   <td colname="col2"> <p>横幅索引的垂直对齐方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">行高</span> </p> </td> 
   <td colname="col2"> <p>横幅索引的文本高度。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指标项支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于集合中的当前元素；`state="unselected"`对应于默认项目状态。

例如，假设您想在点状模式下为桌面系统设置一个设置指示器。 您希望将其放在距离查看器底部20像素的位置。 并且，您希望未选取的点为黑色，具有50%的透明度，15 x 15像素，具有7个圆角像素。 所选点为黑色，透明度为90%，18 x 18像素为9像素圆角。 点之间的间距为5像素。

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
