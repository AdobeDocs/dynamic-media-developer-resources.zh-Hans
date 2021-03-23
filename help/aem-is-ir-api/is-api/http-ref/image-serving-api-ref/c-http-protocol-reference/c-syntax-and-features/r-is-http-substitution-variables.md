---
description: 替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。
seo-description: 替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。
seo-title: 替换变量
solution: Experience Manager
title: 替换变量
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---


# 替换变量{#substitution-variables}

替换变量用于将值从请求URL传输到图像目录中存储的合成模板。 变量还可用于向复杂请求中的不同位置传递相同的值。

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>变量名称。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>要设置变量的值（字符串）。 </p> </td> 
 </tr> 
</table>

变量定义和引用可能出现在请求的查询部分、`catalog::Modifier`和`catalog::PostModifier`中。

变量定义如上，与其他IS命令类似；前导“$”将命令标识为变量定义。 在引用变量之前，必须定义变量。

变量名&#x200B;*`var`*&#x200B;不区分大小写，可能由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。

>[!NOTE]
>
>*`value`* 必须采用单通URL编码，才能进行安全的HTTP传输。如果通过HTTP重新传输&#x200B;*`value`*，则需要多次编码。 在将&#x200B;*`value`*&#x200B;替换为嵌套外来请求或SVG `<image>`元素的href属性时，会出现这种情况。

变量引用由前导和尾随“$”($*var*$)分隔的变量名组成。 任何IS命令的值部分中的任何位置（即，在命令名称后面的“=”与后续的“&amp;”或请求的结尾之间）都可能发生引用。 无法将自定义变量应用于`layer=`和`effect=`命令。 允许在同一命令值中使用多个变量。 服务器将每次出现的` $ *`var`*$`替换为&#x200B;*`value`*。

变量引用可能未嵌套。 在&#x200B;*`value`*&#x200B;中出现的任何` $ *`var`*$`未替换。

例如，请求片段：

`$var2=apple&$var1=my$var2$tree&text=$var1$`

解析为：

`text=my$var2$tree`

>[!NOTE]
>
>“$”不是保留字符；在请求中可能会发生其他情况。 例如，`src=my$image$file.tif`是一个有效的命令（假定名为`my$image$file.tif`的目录条目或图像文件存在），而`wid=$number$`则不是，因为`wid`需要一个数字参数。

## 嵌套请求{#section-26d63adc446c4fa0808e11e8082abdfa}中的变量处理

` $ *`变`*$` 量引用可能出现在嵌套图像服务或图像渲染请求的花括号内的任何位置，包括“？”左侧将路径与查询分离。 在进一步分析和处理嵌套请求之前，服务器将这些引用替换为值（来自URL或主图像目录的`catalog::Modifier`）。

此外，来自url或`catalog::Modifier`的所有` $ *`var`*=`定义都将转发到所有嵌套的图像服务和图像渲染请求。 这可确保所有模板都可以使用所有变量定义，而不管嵌套级别如何。

无论嵌套级别如何，只能对要在嵌套图像渲染或图像服务请求或其关联的`catalog::Modifier`字符串中的任意位置替换的变量值应用单遍HTTP编码。

## 嵌入式外来请求{#section-314e39a9aefb46faa737fd137897d1b0}中的变量处理

` $ *`嵌`*$` 入的外部请求的花括号内出现的varreferences将替换为匹配的变量定义值。这允许将嵌入的外来请求放置在图像目录中的模板中。

要替换为外部请求的变量值通常必须进行多次编码，因为在服务器尝试传输最终的外部url之前，不会应用重新编码。

## SVG文件{#section-a8359f9909764142b6a18ae778dca913}中的变量处理

` $ *`SVG文`*$` 件在属性值和字符串中可能会出现 `<text>` 变量引用。“图像服务”用在指定SVG文件的请求嵌套级别上已知的匹配` $ *`var`*=`定义替换这些定义。

>[!NOTE]
>
>要替换为`href`属性值的任何变量值都必须采用多次URL编码；其他所有项目都必须单独编码。

## 预定义路径变量{#section-930d0dd12e8f49499becc9fe8df24092}

在请求路径中指定的&#x200B;*`object`*&#x200B;将分配给预定义变量`*`$object`*`。 “ ` $ *`object`*$`”可以放置在请求中、请求引用的模板中或允许此类对象的嵌套/嵌入请求中的任意位置，包括`src=`和`mask=`的值以及嵌套/嵌入请求的路径。

例如，以下请求将重复使用路径中指定的图像作为嵌套请求中图层的源：

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

这等于

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

`*`$object`*`的定义可以通过显式指定具有所需值的` $ *`object`*=`来覆盖。

预定义的路径变量通常与`template=`一起使用。

## 默认 {#section-b02483d15529444586a2e9504805b155}

无. 服务器将仅替换已定义的变量（预定义路径变量$object除外，它将始终被替换）。 如果`*`var`*`不能与现有变量定义匹配，则任何` $ *`var`*$`的匹配项都保留字面。

## 示例 {#section-fba9393df6984247b7e30b3f93992e86}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的“Example A”。

## 另请参阅 {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [模板=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
