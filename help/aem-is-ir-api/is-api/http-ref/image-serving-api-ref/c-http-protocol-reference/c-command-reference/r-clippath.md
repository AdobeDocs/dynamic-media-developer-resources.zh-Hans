---
title: clip路径
description: 图层剪辑路径。 指定当前图层的剪辑路径。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '533'
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

图层中位于`clipPath=`所定义区域之外的任何部分都呈现为透明。

`*`pathName`*`是嵌入到图层源图像中的路径的名称。 路径被自动变换以保持与图像内容的相对对齐。 如果指定了多个`*`pathName`*`，服务器会将图像剪辑到这些路径的交集。 在源映像中未找到任何`*`pathName`*`将被忽略。

>[!NOTE]
>
>`*`pathName`*`仅支持ASCII字符串。

`*`pathDefinition`*`允许以图层像素坐标指定显式路径数据。

如果指定了`size=`而不是0,0，则会保留该层。 在这种情况下，路径坐标相对于图层矩形的左上角，图层将基于`origin=`或其默认值进行定位。 图层矩形之外的路径的任何区域都保持透明。

如果没有为纯色或文本图层指定`size=`，则图层会被视为自调整大小，路径范围将决定其大小。 如果未指定`origin=`，则默认为路径坐标空间的(0,0)。 此工作流流程有效地允许指定相对于第0层原点的路径坐标。

>[!NOTE]
>
>不允许对自调整大小的纯色图层使用`scale=`、`rotate=`和`anchor=`命令。

`*`pathDefinition`*`接受与SVG`<path>`元素的`d=`属性的值类似的字符串，只不过使用逗号而不是空格来分隔值。 `*`pathDefinition`*`可以包含一个或多个闭环子路径。

`*`pathDefinition`*`支持以下路径命令：

<table id="table_A74DD7A48B1C417D9D4BA46BECEAB981"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>命令</b> </th> 
   <th class="entry"> <b>名称</b> </th> 
   <th class="entry"> <b>描述</b> </th> 
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
* 0,0，如果它是第一个子路径。

## 属性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

层属性。 应用于当前图层或复合图像（如果`layer=comp`）。 效果图层忽略它。

如果在图层源映像中未找到具有指定名称的路径，或者图层源不是映像，则忽略修饰符`clipPathE=`。

## 默认 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

无，表示没有附加的图层剪辑。

## 另请参阅 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ， [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ， [扩展=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
