---
description: 替换变量用于将请求URL中的值传输到图像目录中存储的合成模板。 变量也可用于将相同的值传达给复杂请求中的不同位置。
solution: Experience Manager
title: 替代变量
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 替代变量{#substitution-variables}

替换变量用于将请求URL中的值传输到图像目录中存储的合成模板。 变量也可用于将相同的值传达给复杂请求中的不同位置。

` $ *`变量`*= *`值`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">变量</span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">值</span> </span> </p> </td> 
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

变量定义和引用可能出现在请求的查询部分、`catalog::Modifier`和`catalog::PostModifier`中。

变量的定义如上所述，与其他IS命令类似；前导“$”将该命令标识为变量定义。 必须先定义变量，然后才能引用它们。

变量名称&#x200B;*`var`*&#x200B;不区分大小写，并且可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。

>[!NOTE]
>
>*`value`*&#x200B;必须为单通道URL编码，以便安全HTTP传输。 如果通过HTTP重新传输&#x200B;*`value`*，则需要双重编码。 当&#x200B;*`value`*&#x200B;被替换为嵌套外部请求或SVG `<image>`元素的href属性时，就是这种情况。

变量引用包括由前导和尾随分隔的变量名称“$”($*var*$)。 引用可以出现在任何IS命令的值部分的任何位置（即，在命令名称后面的“=”和后续的“&amp;”或请求结尾之间）。 自定义变量无法应用于`layer=`和`effect=`命令。 同一命令值中允许使用多个变量。 服务器使用` $ *`替换`*$`var *`value`*&#x200B;的每个匹配项。

变量引用不能嵌套。 在` $ *`内出现的`*$`var *`value`*&#x200B;均不会被替换。

例如，请求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析为：

`text=my$var2$tree`

>[!NOTE]
>
>“$”不是保留字符；它可能在请求中出现。 例如，`src=my$image$file.tif`是有效的命令（假定存在名为`my$image$file.tif`的目录条目或图像文件），而`wid=$number$`则否，因为`wid`需要数值参数。

## 嵌套请求中的变量处理 {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$`引用可能出现在嵌套图像服务或图像渲染请求的大括号内的任何位置，包括“？”的左侧 将路径与查询分开。 在进一步解析和处理嵌套请求之前，服务器会将这些引用替换为来自URL或主图像目录的`catalog::Modifier`的值。

此外，URL或` $ *`中的所有`*=`var`catalog::Modifier`定义都将转发到所有嵌套的图像服务和图像渲染请求。 这样可以确保所有变量定义都可用于所有模板，而不管嵌套级别如何。

无论嵌套级别如何，必须只对变量值应用单次HTTP编码，这些变量值将在嵌套图像渲染或图像服务请求或其关联的`catalog::Modifier`字符串中的任意位置被替换。

## 在嵌入的外来请求中进行变量处理 {#section-314e39a9aefb46faa737fd137897d1b0}

在嵌入外部请求的大括号内的任意位置出现的` $ *`var`*$`引用将被匹配的变量定义值替换。 这允许将嵌入的外部请求放置在图像目录的模板中。

要替换到外地请求中的变量值通常必须双重编码，因为在服务器尝试传输最终的外部url之前不会应用重新编码。

## SVG文件中的变量处理 {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$`引用可能出现在属性值和`<text>`字符串的SVG文件中。 图像服务使用在指定SVG文件的请求嵌套级别已知的` $ *`var`*=`匹配定义替换这些定义。

>[!NOTE]
>
>任何要替换为`href`属性值的变量值都必须进行双重URL编码；所有其他变量值都必须进行单次编码。

## 预定义路径变量 {#section-930d0dd12e8f49499becc9fe8df24092}

在请求路径中指定的&#x200B;*`object`*&#x200B;已分配给预定义的变量`*`$object`*`。 “` $ *`对象`*$`”可以放置在请求中的任意位置、请求所引用的模板中或允许此类对象的嵌套/嵌入请求中，包括`src=`和`mask=`的值以及嵌套/嵌入请求的路径。

例如，以下请求重用路径中指定的图像作为嵌套请求中的图层的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

这相当于

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

可以使用所需的值显式指定`*`对象`*`，以覆盖` $ *`$object`*=`的定义。

预定义的路径变量通常与`template=`结合使用。

## 默认 {#section-b02483d15529444586a2e9504805b155}

无。 只有已定义的变量才会被服务器替换（预定义的路径变量$object除外，它始终被替换）。 如果` $ *`var`*$`无法与现有变量定义匹配，则`*`var`*`的任何匹配项均保持为文本。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

请参阅[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的“示例A”。

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)，[模板=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
