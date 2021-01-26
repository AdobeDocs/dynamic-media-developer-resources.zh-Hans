---
description: RTF规范允许使用&bsol;colortbl指定的RGB颜色值。 每个组件分别提供&bsol;red、&bsol;green和&bsol;blue命令。
solution: Experience Manager
title: 颜色处理
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---


# 颜色处理{#color-handling}

RTF规范允许使用`\colortbl`指定的RGB颜色值。 每个组件分别提供`\red`、`\green`和`\blue`命令。

专有RTF扩展命令`\cmykcolortbl`允许指定CMYK颜色，每个颜色组件都提供有`\cyan`、`\magenta`、`\yellow`和`\black`命令。

`\colortbl`的颜色组件值在0到255的范围内。 `\cmykcolortbl`的组件值在0到100的范围内。

RTF扩展命令`\*\iscolortbl`受`textPs=`支持，它提供了一种指定带有标准图像服务颜色值的颜色表的方法，该颜色表完全支持RGB、灰色、CMYK和alpha。 它的语法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一个或多个IS颜色值，用“;”分隔

可以在同一个`text=`或`textPs=` RTF字符串中指定多种类型的颜色表。 每个颜色表可以有不同数量的条目。 图像服务将尝试按以下顺序查找颜色：`\cmykcolortbl`之前的`\iscolortbl`（仅当文本图层的像素类型为CMYK时）在`\colortbl`之前。 仅对`textPs=`，如果需要，颜色在CMYK和RGB之间精确转换（例如，指定RGB颜色但需要CMYK输出时）。 如果找不到特定索引值的颜色，则使用默认颜色（黑色）。

有关IS颜色值语法的说明，请参阅[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制{#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支持 `\*\iscolortbl`。`textPs=` 不支持 `\cmykcolortbl`。

渲染Photofonts时忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
