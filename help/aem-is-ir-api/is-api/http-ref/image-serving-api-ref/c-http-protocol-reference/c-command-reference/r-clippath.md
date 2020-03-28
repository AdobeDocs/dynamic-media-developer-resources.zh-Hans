---
description: 图层剪辑路径。 为当前图层指定剪辑路径。
seo-description: 图层剪辑路径。 为当前图层指定剪辑路径。
seo-title: clipPath
solution: Experience Manager
title: clipPath
topic: Scene7 Image Serving - Image Rendering API
uuid: fe84cf7a-63af-47d3-ae4f-2122f2f0a262
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# clipPath{#clippath}

图层剪辑路径。 为当前图层指定剪辑路径。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span></span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入在图层源图像中的路径的名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

图层中位于由定义的区域之外的任何部分都 `clipPath=` 会变为透明。

` *`pathName`*` 是嵌入在图层源图像中的路径的名称。 自动转换路径以保持与图像内容的相对对齐。 如果指定了多 ` *`个pathName`*` ，则服务器会将图像剪辑到这些路径的交点。 将忽 ` *`略在源图像中找不到的任何pathName`*` 。

>[!NOTE]
>
>pathName仅支持ASCII字 ` *`符串`*`。

` *`pathDefinition允许`*` 在图层像素坐标中指定显式路径数据。

如果 `size=` 指定而非0,0，则定位图层。 在这种情况下，路径坐标是相对于图层矩形的左上角的，并且图层的位置基于或其默 `origin=` 认值。 图层矩形外的路径的任何区域都保持透明。

如果 `size=` 未为纯色或文本图层指定，则将视图层为自调整大小，而路径的范围将决定其大小。 如果 `origin=` 未指定，则默认为路径坐标空间的(0,0)。 这有效地允许相对于图层0的来源指定路径坐标。

>[!NOTE]
>
>`scale=`、 `rotate=`和命令 `anchor=` 不允许对纯色图层进行自调整大小。

` *`pathDefinition接受与SVG元素属性值类似的字符串`*` ，但 `d=``<path>` 是使用逗号而不是空格来分隔值。 ` *`pathDefinition`*` 可以包括一个或多个闭环子路径。

pathDefinition支持以下路径 ` *`命令`*`:

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
   <td> <b> M</b><span class="varname"> x,y</span> </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 在x,y处开始新的子路径。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x,y</span> </td> 
   <td> <p> 相对于 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> 行到绝对 </p> </td> 
   <td> <p> 从当前位置到x,y绘制一条线。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x,y</span>} </td> 
   <td> <p> lineto relative </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 从当前位置到x,y绘制一条贝塞尔曲线。x1,y1是曲线开始处的控制点，x2,y2是曲线结束处的控制点。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x,y</span>} </td> 
   <td> <p> 临时相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> close path </p> </td> 
   <td> <p> 用直线闭合当前子路径。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大写命令表示坐标值位于绝对像素位置（相对于图层矩形的左上角）。 像素偏移量会按照相对于当前位置的小写命令进行操作。

“m”或“M”总是开始新子路径。 如果在末尾未指定“Z”或“z”，则子路径将自动闭合（使用直线）。

如果子路径以相对移动(&#39;m&#39;)开头，则它相对于以下任一方式：

* 前一个子路径的起始点（如果它以“z”或“Z”关闭）。
* 前一个子路径的结束点（如果未显式关闭）。
* 0,0，如果这是第一个子路径。

## 属性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

图层属性。 应用于当前图层或复合图像（如果） `layer=comp`。 效果图层会忽略它。

`clipPathE=` 如果在图层源图像中未找到具有指定名称的路径，或者图层源不是图像，则忽略该路径。

## 默认 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

“无”，因为图层没有其他剪切。

## 另请参阅 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) , [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) , [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
