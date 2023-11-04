---
description: 替换变量用于将请求URL中的值传输到图像目录中存储的合成模板。 变量也可用于将相同的值传达给复杂请求中的不同位置。
solution: Experience Manager
title: 替代变量
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# 替代变量{#substitution-variables}

替换变量用于将请求URL中的值传输到图像目录中存储的合成模板。 变量也可用于将相同的值传达给复杂请求中的不同位置。

` $ *`变量`*= *`值`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 变量 </span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span> </span> </p> </td> 
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

变量定义和引用可能会出现在请求的查询部分中： `catalog::Modifier`、和 `catalog::PostModifier`.

变量的定义如上所述，与其他IS命令类似；前导“$”将该命令标识为变量定义。 必须先定义变量，然后才能引用它们。

变量名称 *`var`* 不区分大小写，并且可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。

>[!NOTE]
>
>*`value`* 必须为单通道URL编码，以便安全HTTP传输。 在以下情况下需要双重编码 *`value`* 通过HTTP重新传输。 以下是示例： *`value`* 被替换为嵌套的外来请求或SVG的href属性 `<image>` 元素。

变量引用包括由前导和尾随分隔的变量名称“$”($)*变量*$)。 引用可以出现在任何IS命令的值部分的任何位置（即，在命令名称后面的“=”和后续的“&amp;”或请求结尾之间）。 自定义变量无法应用于 `layer=` 和 `effect=` 命令。 同一命令值中允许使用多个变量。 服务器替换每次出现的 ` $ *`变量`*$` 替换为 *`value`*.

变量引用不能嵌套。 任何匹配项 ` $ *`变量`*$` 范围 *`value`* 不会被替换。

例如，请求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析为：

`text=my$var2$tree`

>[!NOTE]
>
>“$”不是保留字符；它可能在请求中出现。 例如， `src=my$image$file.tif` 是有效的命令(假定一个目录条目或图像文件名为 `my$image$file.tif` 存在)，而 `wid=$number$` 不是，因为 `wid` 需要数值参数。

## 嵌套请求中的变量处理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`变量`*$` 引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”左侧 将路径与查询分开。 服务器会使用（来自url或的）值替换这些引用 `catalog::Modifier` )，然后进一步解析和处理嵌套请求。

此外，所有 ` $ *`变量`*=` url中的定义或 `catalog::Modifier` 转发到所有嵌套的图像服务和图像渲染请求。 这样可以确保所有变量定义都可用于所有模板，而不管嵌套级别如何。

无论嵌套级别如何，必须只对变量值应用单次HTTP编码，该值将在嵌套图像渲染或图像服务请求或其关联请求中的任意位置被替换 `catalog::Modifier` 字符串。

## 在嵌入的外来请求中进行变量处理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`变量`*$` 在嵌入的外来请求的大括号内的任何位置发生的引用将被匹配的变量定义值替换。 这允许将嵌入的外部请求放置在图像目录的模板中。

要替换到外地请求中的变量值通常必须双重编码，因为在服务器尝试传输最终的外部url之前不会应用重新编码。

## SVG文件中的变量处理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`变量`*$` 引用可能会出现在属性值中的SVG文件和 `<text>` 字符串。 图像服务使用匹配项替换这些项 ` $ *`变量`*=` 在指定SVG文件的请求嵌套级别已知的定义。

>[!NOTE]
>
>要替换为 `href` 属性值必须为双精度URL编码；所有其他值必须为单精度。

## 预定义路径变量 {#section-930d0dd12e8f49499becc9fe8df24092}

此 *`object`* 在请求路径中指定的分配给预定义变量 `*`$object`*`. ’ ` $ *`对象`*$`&#39;可放置在请求中的任意位置、请求引用的模板中，或允许此类对象的嵌套/嵌入请求中，其中包括的值 `src=` 和 `mask=`以及嵌套/嵌入请求的路径。

例如，以下请求重用路径中指定的图像作为嵌套请求中的图层的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

这相当于

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

的定义 `*`$object`*` 可以通过显式指定 ` $ *`对象`*=` ，则返回所需的值。

预定义的路径变量通常与 `template=`.

## 默认 {#section-b02483d15529444586a2e9504805b155}

无. 只有已定义的变量才会被服务器替换（预定义的路径变量$object除外，它始终被替换）。 任何匹配项 ` $ *`变量`*$` 在以下情况下保持文本： `*`变量`*`无法与现有变量定义匹配。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

请参阅中的“示例A” [模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)， [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
