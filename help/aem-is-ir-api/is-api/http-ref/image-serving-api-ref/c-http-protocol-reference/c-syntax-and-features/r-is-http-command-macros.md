---
description: 命令宏为命令集提供命名的快捷键。 宏在单独的宏定义文件中定义，这些文件可附加到图像目录或默认目录。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# 命令宏{#command-macros}

命令宏为命令集提供命名的快捷键。 宏在单独的宏定义文件中定义，这些文件可附加到图像目录或默认目录。

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 名称</span></span> </p> </td> 
  <td class="stentry"> <p>宏名称。 </p></td> 
 </tr> 
</table>

`*`名`*` 称不区分大小写，并且可能由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成字符.

可以在“？”之后的请求中的任意位置以及`catalog::Modifier`或`catalog::PostModifier`字段中的任意位置调用宏。 宏只能表示一个或多个完整的图像服务命令，并且必须与具有“&amp;”分隔符的其他命令分开。

在分析的早期，宏调用会被替换字符串替换。 如果宏中的命令在请求中调用宏之前发生，则它们将覆盖请求中的相同命令。 这与`catalog::Modifier`不同，其中请求字符串中的命令始终会覆盖`catalog::Modifier`字符串中的命令，而与请求中的位置无关。

命令宏不能有参数值，但可以使用自定义变量将值从请求传递到宏。

宏可以嵌套，但有以下限制：只有在分析宏定义时已定义宏时，才能调用宏，方法是在同一宏定义文件中显示得更早，或将此类嵌入宏的定义放入默认宏定义文件中。

## 示例 {#section-2f73d36ac8d64254a03bae5afeae2fb9}

如果要将相同属性应用于不同的图像，则宏可能很有用。

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

我们可以为常见属性定义一个宏：

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

宏的用法如下：

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

由于第三个请求的`wid=`不同，我们只需在调用宏&#x200B;*之后覆盖值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;将不会产生任何效果）。

## 另请参阅 {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), Macro Definition  [Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
