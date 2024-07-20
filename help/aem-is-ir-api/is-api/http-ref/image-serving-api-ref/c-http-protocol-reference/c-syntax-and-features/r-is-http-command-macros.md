---
title: 命令宏
description: 命令宏为命令集提供命名快捷键。 宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏为命令集提供命名快捷键。 宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。

`$ *`名称`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">名称</span></span> </p> </td> 
  <td class="stentry"> <p>宏名称。 </p></td> 
 </tr> 
</table>

`*`name`*`不区分大小写，并且可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成 个字符。

宏可以在“？”之后的请求中任何位置调用，也可以在`catalog::Modifier`或`catalog::PostModifier`字段中的任何位置调用。 宏只能表示一个或多个完整的图像提供命令，并且必须使用`&`分隔符与其他命令分开。

在解析过程中，宏调用在早期被替换字符串替换。 如果宏中的命令发生在请求中的宏调用之前，则宏中的命令会覆盖请求中的相同命令。 此处理流程不同于`catalog::Modifier`，其中请求字符串中的命令始终会覆盖`catalog::Modifier`字符串中的命令，无论请求中的位置如何。

命令宏不能有参数值，但自定义变量可用于将请求中的值传递到宏中。

宏可以嵌套。 但是，只有在宏定义被解析时已定义时，才能调用该宏。 此工作流程可通过以下方法完成：先在同一宏定义文件中显示，或将此类嵌入宏的定义置于默认宏定义文件中。

## 示例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果将相同的属性应用到不同的图像，则宏会很有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

您可以为公共属性定义宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的使用方式如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

由于第三个请求的`wid=`不同，您只需在&#x200B;*之后覆盖值*&#x200B;即可调用宏（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;无效）。

## 另请参阅 {#section-8cdba0ed2480444ca61e719e54f8871c}

[目录：：MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ，[目录：：Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md)，[宏定义引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
