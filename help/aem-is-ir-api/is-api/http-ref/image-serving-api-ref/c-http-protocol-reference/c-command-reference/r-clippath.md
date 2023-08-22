---
title: clip路径
description: 图层剪辑路径。 指定当前图层的剪辑路径。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 0%

---

# clip路径{#clippath}

图层剪辑路径。 指定当前图层的剪辑路径。

`clipPath= *`pathDefinition`*`

`clipPathE= *`pathName`*&#42;[, *`pathName`*]`

<table id="simpletable_275E2A5FAB804C6388BD110D2ACA3C82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathDefinition</span> </span> </p> </td> 
  <td class="stentry"> <p>路径数据。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pathName</span></span> </p> </td> 
  <td class="stentry"> <p>嵌入到图层源图像中的路径的名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

图层中位于由定义的区域之外的任何部分 `clipPath=` 将渲染为透明。

`*`pathName`*` 是嵌入到图层源图像中的路径的名称。 路径被自动变换以保持与图像内容的相对对齐。 如果有多个 `*`pathName`*` 指定后，服务器将图像裁剪到这些路径的交点。 任何 `*`pathName`*` 在源映像中未找到将忽略。

>[!NOTE]
>
>仅支持ASCII字符串 `*`pathName`*`.

`*`pathDefinition`*` 允许以图层像素坐标指定显式路径数据。

如果 `size=` 指定而非0,0，则会使层保持原样。 在这种情况下，路径坐标相对于图层矩形的左上角，并且图层定位基于 `origin=` 或其默认值。 图层矩形之外的路径的任何区域都保持透明。

如果 `size=` 未指定纯色或文本图层，该图层会被视为自调整大小，路径范围将决定其大小。 如果 `origin=` 未指定，则默认为路径坐标空间的(0,0)。 这实际上允许指定相对于图层0原点的路径坐标。

>[!NOTE]
>
>`scale=`， `rotate=`、和 `anchor=` 不允许对纯色图层进行自调整大小命令。

`*`pathDefinition`*` 接受一个字符串，它与 `d=` SVG的属性 `<path>` 元素，只不过使用逗号而不是空格来分隔值。 `*`pathDefinition`*` 可以包括一个或多个闭环子路径。

中支持以下路径命令 `*`pathDefinition`*`：

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
   <td> <b> M</b> <span class="varname"> x，y</span> </td> 
   <td> <p> moveto absolute </p> </td> 
   <td> <p> 在x，y处开始新的子路径。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> m</b> <span class="varname"> x，y</span> </td> 
   <td> <p> 相对移动 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 从直线到绝对 </p> </td> 
   <td> <p> 绘制一条从当前位置到x，y的直线。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 直线对相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1，y1，x2，y2，x，y</span>} </td> 
   <td> <p> curveto absolute </p> </td> 
   <td> <p> 绘制一条从当前位置到x，y的贝塞尔曲线，其中x1，y1是曲线开头的控制点，x2，y2是曲线结尾的控制点。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1，y1，x2，y2，x，y</span>} </td> 
   <td> <p> curveto相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b> | <b>z</b> </td> 
   <td> <p> closepath </p> </td> 
   <td> <p> 使用直线关闭当前子路径。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大写命令指示坐标值位于绝对像素位置（相对于图层矩形左上角）。 相对于当前位置，像素偏移跟随小写命令。

“M”或“M”始终启动新的子路径。 如果在末尾未指定“Z”或“z”，则子路径将自动关闭（使用直线）。

如果子路径以相对移动量(“m”)开头，则它相对于以下项之一：

* 上一个子路径的起点（如果以“z”或“Z”结尾）。
* 上一个子路径的终点（如果未显式关闭）。
* 0,0（如果这是第一个子路径）。

## 属性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

层属性。 应用到当前图层或复合图像，如果 `layer=comp`. 效果图层忽略它。

`clipPathE=` 如果在图层源映像中未找到具有指定名称的路径，或者图层源不是映像，则忽略该路径。

## 默认 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

无，表示没有附加的图层剪辑。

## 另请参阅 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ， [文本流路径=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
