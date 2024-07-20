---
title: 设置指示器
description: 设置指示器是在触摸设备上使用查看器时，在主样本上方呈现的一系列点。 当滚动按钮不可用时，圆点可帮助用户浏览缩略图页面。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 53ee058a-cb8c-4b1f-bb9b-caaecc12c947
source-git-commit: cdc85af782ebc492ae2303469a7f4f54b5bc09c8
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 0%

---

# 设置指示器{#set-indicator}

设置指示器是在触摸设备上使用查看器时，在主样本上方呈现的一系列点。 当滚动按钮不可用时，圆点可帮助用户浏览缩略图页面。

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

设置指示器的&#x200B;**CSS属性**

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
   <td colname="col1"> <p> <span class="codeph">背景色</span> </p> </td> 
   <td colname="col2"> <p>设置指示器的十六进制格式的背景颜色。 </p> </td> 
  </tr> 
 </tbody> 
</table>

示例 — 创建具有白色背景的设置指示器：

```
.s7mixedmediaviewer .s7setindicator { 
 background-color: #FFFFFF; 
}
```

单个设置指示符点的外观由CSS类选择器控制：

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
 </tbody> 
</table>

>[!NOTE]
>
>设置指示符点支持`state`属性选择器，该选择器可用于将不同的外观应用于不同的缩略图状态。 特别是，`state="selected"`对应于当前缩略图页面，`state="unselected"`对应于默认点状态。

示例 — 要创建一个15 x 15像素的设置指示器点，该点具有两个像素水平边距、五个像素上边距、一个像素下边距、12像素半径、#D5D3D3种默认颜色和#939393种活动颜色：

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
