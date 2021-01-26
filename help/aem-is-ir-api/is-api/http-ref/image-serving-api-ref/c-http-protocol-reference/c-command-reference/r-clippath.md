---
description: 图层剪辑路径。 指定当前图层的剪辑路径。
seo-description: 图层剪辑路径。 指定当前图层的剪辑路径。
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 1%

---


# clipPath{#clippath}

图层剪辑路径。 指定当前图层的剪辑路径。

`clipPath= *`pathDefinition`*`

`clipPathE= *``*&#42;[, *`pathNamepathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入在层源图像中的路径名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

位于由`clipPath=`定义的区域之外的图层的任何部分都呈现为透明。

`*``*` pathName是嵌入在图层源图像中的路径的名称。自动转换路径以保持与图像内容的相对对齐。 如果指定了多个`*`pathName`*`，则服务器会将图像剪辑到这些路径的交叉点。 忽略源映像中未找到的任何`*`pathName`*`。

>[!NOTE]
>
>`*`pathName`*`仅支持ASCII字符串。

`*`pathDefinition`*` 允许在图层像素坐标中指定显式路径数据。

如果指定了`size=`而未指定0,0，则保留层。 在这种情况下，路径坐标是相对于图层矩形的左上角的，并且该图层基于`origin=`或其默认值进行定位。 层矩形外的路径的任何区域都保持透明。

如果未为纯色或文本图层指定`size=`，则会将图层视为自调整大小，其大小取决于路径的大小。 如果未指定`origin=`，则它默认为路径坐标空间的(0,0)。 这有效地允许相对于层0的来源指定路径坐标。

>[!NOTE]
>
>`scale=`、 `rotate=`和命 `anchor=` 令不允许对实色图层进行自调整大小。

`*`pathDefinition`*` 接受一个与SVG元素属 `d=` 性值类似的 `<path>` 字符串，不同之处在于使用逗号而不是空格来分隔值。`*``*` pathDefinition可以包括一个或多个闭环子路径。

`*`pathDefinition`*`支持以下路径命令：

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 命令</b> </th> 
   <th class="entry"> <b> 名称</b> </th> 
   <th class="entry"> <b> 说明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> Mx,y</span> </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 开始x,y处的新子路径。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx,y</span> </td> 
   <td> <p> 相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 行至绝对 </p> </td> 
   <td> <p> 从当前位置绘制一条线到x,y。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 线到相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 绘制一条从当前位置到x,y的贝塞尔曲线。x1,y1是曲线开始处的控制点，x2,y2是曲线结束处的控制点。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> |  <b>z</b> </td> 
   <td> <p> 近路 </p> </td> 
   <td> <p> 用直线关闭当前子路径。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大写命令表示坐标值位于绝对像素位置（相对于图层矩形的左上角）。 像素偏移量会遵循相对于当前位置的小写命令。

“m”或“M”总是开始新子路径。 如果末尾未指定“Z”或“z”，则子路径将自动关闭（用直线）。

如果子路径以相对移动(“m”)开头，则它相对于以下任一方式：

* 上一个子路径的起始点（如果它以“z”或“Z”关闭）。
* 上一个子路径的结束点（如果它未显式关闭）。
* 0,0，如果这是第一个子路径。

## 属性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

图层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 效果图层会忽略它。

`clipPathE=` 如果在图层源图像中未找到具有指定名称的路径，或者图层源不是图像，则忽略该路径。

## 默认 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

无，不附加图层剪切。

## 另请参阅 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
