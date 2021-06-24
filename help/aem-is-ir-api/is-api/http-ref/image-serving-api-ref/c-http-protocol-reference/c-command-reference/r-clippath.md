---
description: 图层剪辑路径。 指定当前图层的剪辑路径。
solution: Experience Manager
title: clipPath
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 86c87cd1-6e08-40cb-80e6-35a9f49b6572
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '549'
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
  <td class="stentry"> <p>层源图像中嵌入的路径的名称（仅限ASCII）。 </p></td> 
 </tr> 
</table>

位于`clipPath=`所定义区域之外的层的任何部分都呈现为透明。

`*``*` pathName是嵌入在层源图像中的路径的名称。自动地转换路径以保持与图像内容的相对对准。 如果指定了多个`*`pathName`*`，则服务器会将图像剪辑到这些路径的交集。 在源映像中找不到的任何`*`pathName`*`都将被忽略。

>[!NOTE]
>
>`*`pathName`*`仅支持ASCII字符串。

`*``*` pathDefinition允许在层像素坐标中指定显式路径数据。

如果指定了`size=`而未指定0,0，则会定位层。 在这种情况下，路径坐标相对于层矩形的左上角，并且层基于`origin=`或其缺省位置进行定位。 层矩形外路径的任何区域都保持透明。

如果未为纯颜色或文本层指定`size=`，则该层会被视为自调整大小，并由路径的范围确定其大小。 如果未指定`origin=`，则默认为(0,0)路径坐标空间。 这有效地允许相对于层0的原点指定路径坐标。

>[!NOTE]
>
>`scale=`、和 `rotate=`命 `anchor=` 令不允许对实色图层进行自调整大小。

`*``*` pathDefinition接受与SVG元素属性值类 `d=` 似的字 `<path>` 符串，不同之处在于使用逗号而不是空格来分隔值。`*``*` pathDefinition可以包含一个或多个闭环子路径。

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
   <td> <b> </b> <span class="varname"> Mx，y</span> </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 在x，y处启动新子路径。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> </b> <span class="varname"> mx，y</span> </td> 
   <td> <p> 相对 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> L</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 行到绝对 </p> </td> 
   <td> <p> 从当前位置绘制一条线到x，y。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> l</b> *{<span class="varname"> x，y</span>} </td> 
   <td> <p> 相对行 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> C</b> *{<span class="varname"> x1,y1,x2,y2,x，y</span>} </td> 
   <td> <p> 绝对 </p> </td> 
   <td> <p> 将贝塞尔曲线从当前位置绘制为x，y。x1,y1是曲线开头的控制点，x2,y2是曲线末尾的控制点。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> c</b> *{<span class="varname"> x1,y1,x2,y2,x，y</span>} </td> 
   <td> <p> 相对于 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <b> Z</b>  |  <b>z</b> </td> 
   <td> <p> 闭合路径 </p> </td> 
   <td> <p> 使用直线关闭当前子路径。 </p> </td> 
  </tr> 
 </tbody> 
</table>

大写命令表示坐标值位于绝对像素位置（相对于图层矩形的左上角）。 像素偏移会遵循相对于当前位置的小写命令。

“m”或“M”始终启动新子路径。 如果未在末尾指定“Z”或“z”，则子路径将自动关闭（使用直线）。

如果子路径以相对移动(“m”)开头，则它相对于以下任一路径：

* 上一个子路径的起始点（如果它以“z”或“Z”关闭）。
* 上一个子路径的结束点（如果未明确关闭）。
* 0,0，如果这是第一个子路径。

## 属性 {#section-d4127db0dac54e3cbd44f7ea1e001960}

层属性。 应用于当前层或复合图像（如果`layer=comp`）。 效果层会忽略它。

`clipPathE=` 如果在层源图像中未找到具有指定名称的路径，或者层源不是图像，则忽略该路径。

## 默认 {#section-076c35ea37fa4a44ada253b4c2dec1dd}

“无”(None)，表示图层没有额外的剪切。

## 另请参阅 {#section-dd8110fb6f5c45eba6284c5ec5f49056}

[clipXpath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clipxpath.md#reference-17e5e4da3e044943af8f963f58a45f53) ,  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef) ,  [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
