---
description: 设置指示符是在触控设备上使用查看器时在色板上呈现的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩略图的页面中导航。
seo-description: 设置指示符是在触控设备上使用查看器时在色板上呈现的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩略图的页面中导航。
seo-title: 设置指示符
solution: Experience Manager
title: 设置指示符
topic: Dynamic media
uuid: 802916a6-cec5-469b-b54c-dd379925a8c2
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# 设置指示符{#set-indicator}

设置指示符是在触控设备上使用查看器时在色板上呈现的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩略图的页面中导航。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示符的CSS属性**

设置指示符容器的外观由以下CSS类选择器控制：

```
.s7zoomviewer .s7setindicator
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
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>设置指示符的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例——设置具有白色背景的设置指示符：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

使用CSS类选择器控制单个设置指示符点的外观：

`.s7zoomviewer .s7setindicator .s7dot`

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
   <td colname="col1"> <p> <span class="codeph"> margin-left </span> </p> </td> 
   <td colname="col2"> <p>左边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-top </span> </p> </td> 
   <td colname="col2"> <p>上边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> margin-right </span> </p> </td> 
   <td colname="col2"> <p>右边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 边距——底部 </span> </p> </td> 
   <td colname="col2"> <p>底边距（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border-radius </span> </p> </td> 
   <td colname="col2"> <p>边框半径（以像素为单位）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景颜色 </span> </p> </td> 
   <td colname="col2"> <p>十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符点支持属 `state` 性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是， `state="selected"` 与缩略图的当前页面对应， `state="unselected"` 与默认的点状态对应。

示例——将设置的指示符点设置为15 x 15像素，带有两个像素的水平边距、五个像素的上边距、一个像素的底边距、十二个像素的半径、#D5D3D3默认颜色和#939393活动颜色：

```
.s7zoomviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7zoomviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```

