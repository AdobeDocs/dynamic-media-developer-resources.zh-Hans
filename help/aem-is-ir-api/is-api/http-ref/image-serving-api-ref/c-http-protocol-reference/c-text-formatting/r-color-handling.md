---
description: RTF规范允许使用&bsol;colortbl指定的RGB颜色值。 每个组件分别提供&bsol;red、&bsol;green和&bsol;blue命令。
solution: Experience Manager
title: 颜色处理
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# 颜色处理{#color-handling}

RTF规范允许使用`\colortbl`指定的RGB颜色值。 每个组件分别提供了`\red`、`\green`和`\blue`命令。

专有的RTF扩展命令`\cmykcolortbl`允许指定CMYK颜色，每个颜色组件都提供了`\cyan`、`\magenta`、`\yellow`和`\black`命令。

`\colortbl`的颜色分量值在0到255之间。 `\cmykcolortbl`的组件值在0到100之间。

`textPs=`支持的RTF扩展命令`\*\iscolortbl`提供了一种方法，用于指定支持全RGB、灰色、CMYK和Alpha的标准图像服务颜色值的颜色表。 其语法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一个或多个IS颜色值，以“；”分隔

可以在同一个`text=`或`textPs=` RTF字符串中指定多种类型的颜色表。 每个颜色表可以具有不同的条目数。 图像提供将尝试按以下顺序查找颜色：`\iscolortbl`之前的`\cmykcolortbl`（仅当文本层的像素类型为CMYK时）。 `\colortbl`仅对于`textPs=`，如果需要，颜色会在CMYK和RGB之间准确转换（例如，当指定了RGB颜色但需要CMYK输出时）。 如果未找到特定索引值的颜色，则使用默认颜色（黑色）。

有关IS颜色值语法的说明，请参阅[color](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支持 `\*\iscolortbl`。`textPs=` 不支持 `\cmykcolortbl`。

在渲染Photofonts时，颜色选择会被忽略。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
