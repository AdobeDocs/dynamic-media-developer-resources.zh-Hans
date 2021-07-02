---
description: 设置指示器是在触控设备上使用查看器时，在主色板上呈现的一系列点。 当滚动按钮不可用时，这些圆点图可帮助用户在缩略图的页面中导航。
solution: Experience Manager
title: 设置指示器
feature: Dynamic Media Classic，查看器，SDK/API，混合媒体集
role: Developer,Business Practitioner
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# 设置指示器{#set-indicator}

设置指示器是在触控设备上使用查看器时，在主色板上呈现的一系列点。 当滚动按钮不可用时，这些圆点图可帮助用户在缩略图的页面中导航。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**设置指示器的CSS属性**

使用以下CSS类选择器控制设置指示器容器的外观：

```
.s7mixedmediaviewer .s7setindicator
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

示例 — 要设置带白色背景的设置指示器：

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示器点的外观由CSS类选择器控制：

`.s7mixedmediaviewer .s7setindicator .s7dot`

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
 </tbody> 
</table>

>[!NOTE]
>
>设置指示器点支持`state`属性选择器，该选择器可用于将不同的外观应用到不同的缩略图状态。 特别是，`state="selected"`对应于当前的缩略图页面，`state="unselected"`对应于默认的点状态。

示例 — 将指示器点设置为15 x 15像素，其中包含两个像素水平边距、五个像素顶边距、一个像素底边距、十二个像素半径、默#D5D3D3颜色和#939393活动颜色：

```
.s7mixedmediaviewer .s7setindicator .s7dot { 
 width:15px; 
 height:15px; 
 margin-left:2px; 
 margin-top:5px; 
 margin-right:2px; 
 margin-bottom:1px; 
 border-radius:12px; 
 background-color:#D5D3D3;  
} 
.s7mixedmediaviewer .s7setindicator .s7dot[state="selected"] { 
 background-color:#939393;  
}
```
