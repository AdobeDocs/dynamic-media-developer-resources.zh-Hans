---
description: 选择“图层”。 选择一个图层，并在命令序列中开始新的图层定义段。
seo-description: 选择“图层”。 选择一个图层，并在命令序列中开始新的图层定义段。
seo-title: 层
solution: Experience Manager
title: 层
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 882309b3-51d7-477e-bd09-068ce9e55eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 1%

---


# 层{#layer}

选择“图层”。 选择一个图层，并在命令序列中开始新的图层定义段。

`layer= *`名`*|comp[, *`称`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要选择的层数（0或更大的int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>选择复合图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名称</span></span> </p></td> 
  <td class="stentry"> <p>图层名称. </p></td> 
 </tr> 
</table>

层段内的所有命令都应用于指定的层。 层段由下一个`layer=`或`effect=`命令或请求的结束终止。

指定`layer=comp`以选择复合图像(或视图，对于某些命令)。

图层编号有效地指定图层的z顺序。 编号较高的图层放置在编号较低的图层的顶部。

图层编号不需要是连续的。 第0层是必需的。

可以将名称分配给具有`layer= *`n`*, *`name`*`命令变体的层。 定义命名层后，可以使用` layer= *`name`*`引用它，无需知道层号。 可使用多个`layer= *`n`*, *`name`*`命令将多个名称分配给同一层。

>[!NOTE]
>
>第0层决定合成画布的总体大小。 在构建复合图像时，将裁切掉位于图层0边界之外的所有图层部分。

## 属性 {#section-499963ee52c14f2898f0d0f90c1d01be}

图层命令。 `layer=`中不支持替代变量引用。

`comp` 不允许使用字符串 *`name`* 形式。如果将同一个&#x200B;*`name`*&#x200B;分配给多个层，或者如果某个层被&#x200B;*`name`*&#x200B;引用，则返回错误，该层之前尚未定义。

## 默认 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果`layer=comp`，许多命令和属性将应用于层0。

## 特殊情况{#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果同一名称被映射到多个图层(例如：`layer=1,image&layer=2,image`)，出现错误。
* 如果同一名称多次映射到单个图层(例如：`layer=1,image&layer=1,image`)，范围设置为正常，没有错误。
* 支持同一图层的多个名称。

   任一名称都可用于引用层(例如：`layer=1,image&layer=1,picture`)。
* 如果引用的名称从未映射到图层编号(例如：`layer=1,image&layer=picture`)，出现错误。
* 图层修饰符中不支持替换变量(例如：`layer=$image$`)。

   这适用于所有排列，不仅适用于图层名称，而且通常也适用于图层修饰符。

* 所有合并和覆盖规则应与在多个源中引用同一层（请求、修改前或修改后目录记录、宏等）时完全相同。

## 示例 {#section-cc40de6a0a754178aa752601539c815b}

请参见[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例。
