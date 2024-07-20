---
title: 颜色处理
description: RTF规范允许使用&amp；bsol；colortbl指定的RGB颜色值。 每个组件分别提供了&amp；bsol；红色、&amp；bsol；绿色和&amp；bsol；蓝色命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# 颜色处理{#color-handling}

RTF规范允许使用`\colortbl`指定的RGB颜色值。 每个组件分别提供了`\red`、`\green`和`\blue`命令。

专用RTF扩展命令`\cmykcolortbl`允许指定CMYK颜色，每个颜色组件都随`\cyan`、`\magenta`、`\yellow`和`\black`命令提供。

`\colortbl`的颜色组件值在0-255范围内。 `\cmykcolortbl`的组件值在0-100范围内。

`textPs=`支持的RTF扩展命令`\*\iscolortbl`提供了一种方法，用于指定具有标准图像服务颜色值的颜色表，该颜色表支持完整RGB、灰度、CMYK和Alpha。 它具有以下语法：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]*&#x200B;一个或多个IS颜色值，以“；”分隔

可以在同一`text=`或`textPs=` RTF字符串中指定多种类型的颜色表。 每个颜色表可以有不同的条目数。 图像服务尝试在`\colortbl`之前按以下顺序查找颜色： `\iscolortbl`在`\cmykcolortbl`之前（仅当文本图层的像素类型为CMYK时）。 仅对于`textPs=`，如果需要(例如，指定了RGB颜色但需要CMYK输出)，可在CMYK和RGB之间准确地转换颜色。 如果找不到特定索引值的颜色，则使用默认颜色（黑色）。

有关IS颜色值的语法的说明，请参阅[颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修饰符`text=`不支持`\*\iscolortbl`。 修饰符`textPs=`不支持`\cmykcolortbl`。

渲染Photofonts时将忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时当在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
