---
description: 替换变量用于将值从请求URL传输到存储在图像目录中的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。
solution: Experience Manager
title: 替换变量
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# 替换变量{#substitution-variables}

替换变量用于将值从请求URL传输到存储在图像目录中的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。

` $ *`var`*= *`值`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>变量要设置到的值（字符串）。 </p> </td> 
 </tr> 
</table>

变量定义和引用可能会在请求的查询部分(位于 `catalog::Modifier`和 `catalog::PostModifier`.

变量的定义如上所示，与其他IS命令类似；前导“$”将命令标识为变量定义。 变量在被引用之前必须进行定义。

变量名称 *`var`* 不区分大小写，可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。

>[!NOTE]
>
>*`value`* 必须采用单次URL编码，才能进行安全HTTP传输。 如果 *`value`* 通过HTTP重新传输。 这种情况下 *`value`* 被替换为嵌套的外来请求或SVG的href属性 `<image>` 元素。

变量引用由由前导和尾随“$”($)分隔的变量名称组成&#x200B;*var*$)。 任何IS命令的值部分中的任何位置（即，在命令名称后面的“=”和随后的“&amp;”或请求的结尾之间）都可能出现引用。 自定义变量无法应用于 `layer=` 和 `effect=` 中。 同一命令值中允许使用多个变量。 服务器会用 ` $ *`var`*$` with *`value`*.

变量引用可能未嵌套。 发生的任何 ` $ *`var`*$` within *`value`* 未替换。

例如，请求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析为：

`text=my$var2$tree`

>[!NOTE]
>
>“$”不是保留字符；请求中可能会出现其他情况。 例如， `src=my$image$file.tif` 是有效的命令(假定目录条目或图像文件名为 `my$image$file.tif` 存在)，而 `wid=$number$` 不是，因为 `wid` 需要一个数值参数。

## 嵌套请求中的变量处理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 引用可能会在嵌套的“图像提供”或“图像呈现”请求的大括号内的任何位置出现，包括位于“？”左侧 将路径与查询分开。 服务器会将这些引用替换为值(从url或从 `catalog::Modifier` 主图像目录)，然后再进一步解析和处理嵌套请求。

此外， ` $ *`var`*=` url或 `catalog::Modifier` 会转发到所有嵌套的图像提供和图像呈现请求。 这可确保所有变量定义都可用于所有模板，而不考虑嵌套级别。

无论嵌套级别如何，都只能对变量值应用单次传递HTTP编码，这些变量值将被嵌套图像渲染或图像服务请求或其关联的任意位置替换 `catalog::Modifier` 字符串。

## 嵌入式外来请求中的变量处理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` 嵌入的外来请求的大括号内出现的引用将被匹配的变量定义值替换。 这允许将嵌入的外来请求放置在图像目录的模板中。

要替换为外来请求的变量值通常必须进行双重编码，因为在服务器尝试传输最终外来URL之前，不会应用重新编码。

## SVG文件中的变量处理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 在属性值和中的SVG文件中可能会发生引用 `<text>` 字符串。 图像服务会将这些值替换为匹配的 ` $ *`var`*=` 在指定SVG文件的请求嵌套级别已知的定义。

>[!NOTE]
>
>要替换为 `href` 属性值必须采用双重URL编码；所有其他内容必须单独编码。

## 预定义路径变量 {#section-930d0dd12e8f49499becc9fe8df24092}

的 *`object`* 在请求路径中指定的变量将分配给预定义的变量 `*`$object`*`. &#39; ` $ *`对象`*$`“ ”可置于请求、请求引用的模板或允许此类对象的嵌套/嵌入请求中的任意位置，包括的值 `src=` 和 `mask=`，以及嵌套/嵌入请求的路径。

例如，以下请求将重复使用路径中指定的图像作为嵌套请求中层的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

这等同于

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

的定义 `*`$object`*` 可以通过显式指定 ` $ *`对象`*=` 值。

预定义路径变量通常与 `template=`.

## 默认 {#section-b02483d15529444586a2e9504805b155}

无. 只有已定义的变量会被服务器替换（预定义的路径变量$object除外，该变量将始终被替换）。 发生的任何 ` $ *`var`*$` 保持原文 `*`var`*`无法与现有变量定义匹配。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

请参阅 [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
