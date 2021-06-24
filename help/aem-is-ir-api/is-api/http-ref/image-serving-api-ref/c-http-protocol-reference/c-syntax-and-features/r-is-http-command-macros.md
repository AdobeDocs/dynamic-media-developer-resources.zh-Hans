---
description: 命令宏为命令集提供了命名的快捷键。 宏在单独的宏定义文件中定义，这些文件可附加到图像目录或默认目录。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏为命令集提供了命名的快捷键。 宏在单独的宏定义文件中定义，这些文件可附加到图像目录或默认目录。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>宏名称。 </p></td> 
 </tr> 
</table>

`*``*` 名称不区分大小写，可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成。字符.

可以在“？”之后的请求中的任意位置以及`catalog::Modifier`或`catalog::PostModifier`字段中的任意位置调用宏。 宏只能表示一个或多个完整的图像服务命令，并且必须与具有“&amp;”分隔符的其他命令分开。

在解析期间，宏调用会被其替换字符串提前替换。 如果宏中的命令在请求中的宏调用之前发生，则它们将覆盖请求中的相同命令。 这与`catalog::Modifier`不同，在中，请求字符串中的命令将始终覆盖`catalog::Modifier`字符串中的命令，而不管请求中的位置如何。

命令宏不能具有参数值，但可以使用自定义变量将值从请求传递到宏。

可以嵌套宏，但存在以下限制：只有在分析宏定义时已经定义宏时，才能调用该宏，方法是先在同一宏定义文件中显示，或者将此类嵌入宏的定义置于默认宏定义文件中。

## 示例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果将相同的属性应用于不同的图像，则宏会非常有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我们可以为常用属性定义一个宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

由于第三个请求的`wid=`不同，因此我们只需在调用宏的&#x200B;*之后覆盖值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;将不会产生任何影响）。

## 另请参阅 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md),  [Macro Definition Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
