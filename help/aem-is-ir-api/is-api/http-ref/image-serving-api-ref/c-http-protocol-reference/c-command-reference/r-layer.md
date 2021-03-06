---
title: 层
description: 选择“图层”。 在命令序列中选择一个层并启动新的层定义段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f1200d86-d88c-4990-ae36-2ce96ae94343
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 1%

---

# 层{#layer}

选择“图层”。 在命令序列中选择一个层并启动新的层定义段。

`layer= *`n`*|comp[, *`name`*]`

`layer= *`name`*`

<table id="simpletable_22DE3365A6454949B0D30C6D7110476E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> n</span></span> </p></td> 
  <td class="stentry"> <p>要选择的层数（0或更大整数）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> comp</span> </p></td> 
  <td class="stentry"> <p>选择复合图像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p></td> 
  <td class="stentry"> <p>图层名称. </p></td> 
 </tr> 
</table>

层段内的所有命令都应用于指定层。 层段由下一层 `layer=` 或 `effect=` 命令或请求的结尾。

指定 `layer=comp` 选择复合图像（或为某些命令选择视图）。

层数有效地指定层的z顺序。 较高编号的图层放置在较低编号的图层的顶部。

层数不必是连续的。 需要第0层。

可以将名称指定给具有 `layer= *`n`*, *`name`*` 命令变量。 定义命名层后，可以通过 ` layer= *`name`*`，而无需知道层号。 可使用多个名称将多个名称分配给同一层 `layer= *`n`*, *`name`*` 中。

>[!NOTE]
>
>第0层确定复合画布的整体大小。 在构建复合材料时，位于层0边界之外的所有层部分都会被裁剪掉。

## 属性 {#section-499963ee52c14f2898f0d0f90c1d01be}

层命令。 不支持替换变量引用 `layer=`.

`comp` 不允许作为 *`name`* 字符串。 如果返回 *`name`* 被分配给多个层，或者如果某个层被 *`name`* 之前未定义。

## 默认 {#section-091859a03f8048c2b7092f0fec9c1006}

`layer=comp`. 如果 `layer=comp`.

## 特殊案件 {#section-e087cb2e3562473e8d391abfa3b9489f}

* 如果同一名称映射到多个层(例如： `layer=1,image&layer=2,image`)，则会出错。
* 如果同一名称多次映射到单个层(例如： `layer=1,image&layer=1,image`)，则照常设置范围，且没有错误。
* 同一层的多个名称受支持。

   任一名称均可用于引用层(例如： `layer=1,image&layer=1,picture`)。
* 如果引用的名称从未映射到层号(例如： `layer=1,image&layer=picture`)，则会出错。
* 层修饰符中不支持替换变量(例如： `layer=$image$`)。

   这适用于所有排列，不仅适用于层名称，还适用于一般的层修饰符。

* 所有合并和覆盖规则应与在多个源（请求、预处理或后处理修饰符目录记录、宏等）中引用同一层时的工作方式完全相同。

## 示例 {#section-cc40de6a0a754178aa752601539c815b}

请参阅 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).
