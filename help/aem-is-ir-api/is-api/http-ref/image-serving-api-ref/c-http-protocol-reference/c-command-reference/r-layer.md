---
title: 图层
description: 选择图层。 选取一个图层并在命令序列中启动一个新的图层定义段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# 图层{#layer}

选择图层。 选取一个图层并在命令序列中启动一个新的图层定义段。

`layer= *`n`*|comp[, *`name`*]`

`layer= *`名称`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要选择的图层数（0或大于int）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>选择复合图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>图层名称。 </p></td> 
 </tr> 
</table>

层段中的所有命令都应用于指定的层。 下一层终止一个层段 `layer=` 或 `effect=` 命令或请求的结尾。

指定 `layer=comp` 以选择复合图像（对于某些命令，选择视图）。

图层编号有效地指定了图层的z顺序。 编号较高的图层位于编号较低的图层之上。

图层编号无需连续。 第0层是必需的。

可以使用为图层指定名称 `layer= *`n`*, *`name`*` 命令变体。 定义命名图层后，可将其引用为 ` layer= *`name`*`，无需知道层数。 可以使用多个名称为同一层指定多个名称 `layer= *`n`*, *`name`*` 命令。

>[!NOTE]
>
>图层0确定合成画布的整体大小。 当复合体构建时，落在层0边界之外的层的全部部分都将被裁剪。

## 属性 {#section-499963ee52c14f2898f0d0f90c1d01be}

“图层”命令。 中不支持替代变量引用 `layer=`.

`comp` 不允许作为 *`name`* 字符串。 如果相同则返回错误 *`name`* 指定给多个图层，或者如果引用了某个图层 *`name`* 之前未定义的属性。

## 默认 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 许多命令和属性都适用于图层0，如果 `layer=comp`.

## 特殊情况 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果将同一名称映射到多个图层(例如： `layer=1,image&layer=2,image`)，出现错误。
* 如果同一个名称多次映射到单个图层(例如： `layer=1,image&layer=1,image`)，范围按常规设置，没有错误。
* 同一层支持多个名称。

   可以使用任一名称来引用层(例如： `layer=1,image&layer=1,picture`)。
* 如果引用的名称从未映射到层编号(例如： `layer=1,image&layer=picture`)，出现错误。
* 层修饰符中不支持替换变量(例如： `layer=$image$`)。

   这适用于所有排列，不仅适用于图层名称，而且适用于一般的图层修饰符。

* 所有合并和覆盖规则的工作方式应与在多个源（请求、前后修饰符目录记录、宏等）中引用同一图层时完全相同。

## 示例 {#section-cc40de6a0a754178aa752601539c815b}

请参阅中的示例 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
