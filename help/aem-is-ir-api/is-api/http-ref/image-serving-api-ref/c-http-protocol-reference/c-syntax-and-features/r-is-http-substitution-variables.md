---
description: 替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。
seo-description: 替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。
seo-title: 替换变量
solution: Experience Manager
title: 替换变量
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 替换变量{#substitution-variables}

替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span></span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值 </span></span> </p> </td> 
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

变量定义和引用可能发生在请求的查询部分、中 `catalog::Modifier`和中 `catalog::PostModifier`。

变量定义如上，与其他IS命令类似；前导“$”将命令标识为变量定义。 变量必须在被引用之前进行定义。

变量名 *`var`* 不区分大小写，可能由ASCII字母、数字、“-”、“_”和“.”的任意组合组成。

>[!NOTE]
>
>*`value`* 必须采用单次URL编码，才能进行安全HTTP传输。 如果通过HTTP重新传输， *`value`* 则需要多次编码。 这种情况下， *`value`* 会被替换为嵌套的外部请求或SVG元素的href属 `<image>` 性。

变量引用由前导和尾部“$”($*var*$)分隔的变量名组成。 任何IS命令的值部分中的任何位置都可能出现引用（即，在命令名称后面的&#39;=&#39;与后续的&#39;&amp;&#39;或请求结束之间）。 自定义变量不能应用于 `layer=` 和命 `effect=` 令。 允许在同一命令值中使用多个变量。 服务器将每次出现的 ` $ *`var替换为`*$`*`value`*。

变量引用不能嵌套。 不替换 ` $ *`任何`*$`*`value`* var的出现。

例如，请求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析到：

`text=my$var2$tree`

>[!NOTE]
>
>“$”不是保留字符；在请求中可能会出现其他情况。 例如，是 `src=my$image$file.tif` 一个有效的命令(假定名为的目录条目或图像文件 `my$image$file.tif` 存在)，而 `wid=$number$` 不是，因为需要 `wid` 一个数字参数。

## 嵌套请求中的变量处理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` 引用可能出现在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“?”左侧 将路径与查询分开。 在进一步分析和处理嵌套请求之前，服务器会将这些引用替换为值( `catalog::Modifier` 来自URL或来自主图像目录)。

此外，URL中的所 ` $ *`有`*=` var定义或URL都会转发 `catalog::Modifier` 到所有嵌套的图像服务和图像渲染请求。 这可确保所有变量定义都对所有模板可用，而不管嵌套级别如何。

无论嵌套级别如何，只能将单遍HTTP编码应用于要在嵌套图像渲染或图像服务请求或其关联字符串中的任意位置替换的变量 `catalog::Modifier` 值。

## 嵌入式外来请求中的变量处理 {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`嵌入`*$` 的外来请求的花括号内出现的var引用将替换为匹配的变量定义值。 这允许将嵌入的外来请求放入图像目录的模板中。

要替换为外来请求的变量值通常必须采用多次编码，因为在服务器尝试传输最终的外来url之前，不会应用重新编码。

## SVG文件中的变量处理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` 引用可能在属性值和字符串中的SVG文件中发 `<text>` 生。 图像服务会用在指定SVG文 ` $ *`件的请求嵌套级别`*=` （已知的匹配var定义）替换这些变量。

>[!NOTE]
>
>任何要替换为属性值的变 `href` 量值都必须采用多次URL编码；其他所有内容都必须单独编码。

## 预定义路径变量 {#section-930d0dd12e8f49499becc9fe8df24092}

请 *`object`* 求路径中指定的变量将分配给预定义的 ` *`变量$object`*`。 “ ` $ *`object`*$`”可以放置在请求中的任意位置、请求引用的模板中或允许此类对象的嵌套／嵌入请求中，包括值和 `src=``mask=`，以及嵌套／嵌入请求的路径。

例如，以下请求将重用路径中指定的图像作为嵌套请求中图层的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

这等同于

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

通过显式指定 ` *`具有所需值的对象`*` ，可以覆 ` $ *`盖$object的定义`*=` 。

预定义的路径变量通常与一起使用 `template=`。

## 默认 {#section-b02483d15529444586a2e9504805b155}

无. 只有已定义的变量会被服务器替换（预定义路径变量$object除外，它将始终被替换）。 如果var与现 ` $ *`有变量定义`*$` ，则任何 ` *``*`var实例都保留为文字。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

请参阅模板中的“示例A [”](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [模板=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
