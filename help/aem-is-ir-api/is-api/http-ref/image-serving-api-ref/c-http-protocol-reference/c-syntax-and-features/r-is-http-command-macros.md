---
description: 命令宏为命令集提供命名快捷键。 宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏为命令集提供命名快捷键。 宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。

`$ *`名称`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>宏名称。 </p></td> 
 </tr> 
</table>

`*`name`*` 不区分大小写，并且可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。 字符.

可以在“？”之后的请求中的任何位置调用宏，也可以在 `catalog::Modifier` 或 `catalog::PostModifier` 字段。 宏只能表示一个或多个完整的图像提供命令，并且必须使用“&amp;”分隔符与其他命令分开。

在解析过程中，宏调用在早期被替换字符串替换。 如果宏中的命令发生在请求中的宏调用之前，则宏中的命令将覆盖请求中的相同命令。 这与不同 `catalog::Modifier`，其中请求字符串中的命令将始终覆盖 `catalog::Modifier` 字符串，而不考虑请求中的位置。

命令宏不能有参数值，但自定义变量可用于将请求中的值传递到宏。

可以嵌套宏，但有下列限制：只有在宏定义解析时已定义宏时，才能调用该宏，方法是在同一宏定义文件中先显示宏，或者在缺省宏定义文件中放置此类嵌入宏的定义。

## 示例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果将相同的属性应用于不同的图像，则宏非常有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我们可以为公共属性定义宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

从 `wid=` 对于第三个请求不同，我们只需覆盖值 *之后* 调用宏(指定 `wid=`*早于* `$view$` 不会产生任何效果)。

## 另请参阅 {#section-8cdba0ed2480444ca61e719e54f8871c}

[目录：：宏文件](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ， [catalog：：Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)， [宏定义引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
