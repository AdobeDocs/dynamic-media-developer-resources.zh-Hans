---
title: 颜色处理
description: RTF规范允许使用&bsol；colortbl指定的RGB颜色值。 每个组件分别提供了&bsol；red、&bsol；green和&bsol；blue命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
TQID: 'https://experienceleague.adobe.com/w5IfFwmdMegueJbDMjwvb5XCPuemRcJ1XTqcJFgdEMQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 颜色处理{#color-handling}

RTF规范允许使用`\colortbl`指定的RGB颜色值。 每个组件分别提供了`\red`、`\green`和`\blue`命令。

专用RTF扩展命令`\cmykcolortbl`允许指定CMYK颜色，每个颜色组件都随`\cyan`、`\magenta`、`\yellow`和`\black`命令提供。

`\colortbl`的颜色组件值在0-255范围内。 `\cmykcolortbl`的组件值在0-100范围内。

`textPs=`支持的RTF扩展命令`\*\iscolortbl`提供了一种方法，用于指定具有标准图像服务颜色值的颜色表，该颜色表支持完整的RGB、灰度、CMYK和Alpha。 它具有以下语法：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]*&#x200B;一个或多个IS颜色值，以“；”分隔

可以在同一`text=`或`textPs=` RTF字符串中指定多种类型的颜色表。 每个颜色表可以有不同的条目数。 图像服务尝试在`\colortbl`之前按以下顺序查找颜色： `\iscolortbl`在`\cmykcolortbl`之前（仅当文本图层的像素类型为CMYK时）。 仅对于`textPs=`，如果需要（例如，当指定了RGB颜色但需要CMYK输出时），可在CMYK和RGB之间准确地转换颜色。 如果找不到特定索引值的颜色，则使用默认颜色（黑色）。

有关IS颜色值的语法的说明，请参阅[颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修饰符`text=`不支持`\*\iscolortbl`。 修饰符`textPs=`不支持`\cmykcolortbl`。

渲染Photofonts时将忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时当在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
