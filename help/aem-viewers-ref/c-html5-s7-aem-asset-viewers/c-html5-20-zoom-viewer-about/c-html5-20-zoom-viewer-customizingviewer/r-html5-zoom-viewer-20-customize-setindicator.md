---
description: 设置指示器是在触控设备上使用查看器时在色板顶部渲染的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩览图页面之间导航。
seo-description: 设置指示器是在触控设备上使用查看器时在色板顶部渲染的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩览图页面之间导航。
seo-title: 设置指示符
solution: Experience Manager
title: 设置指示符
uuid: 802916a6-cec5-469b-b54c-dd379925a8c2
feature: Dynamic Media Classic，查看器，SDK/API，缩放
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 1%

---


# 设置指示符{#set-indicator}

设置指示器是在触控设备上使用查看器时在色板顶部渲染的一系列点。 当滚动按钮不可用时，这些圆点可帮助用户在缩览图页面之间导航。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示符的CSS属性**

使用以下CSS类选择器控制设置指示符容器的外观：

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
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>设置指示符的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 设置白色背景的设置指示符：

```
.s7zoomviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示符点的外观由CSS类选择器控制：

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
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符点支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于当前缩略图页，`state="unselected"`对应于默认点状态。

示例 — 将设置的指示器点设置为15 x 15像素，其中两个像素水平边距、五个像素顶边距、一个像素底边距、十二个像素半径、#D5D3D3默认颜色和#939393活动颜色：

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

