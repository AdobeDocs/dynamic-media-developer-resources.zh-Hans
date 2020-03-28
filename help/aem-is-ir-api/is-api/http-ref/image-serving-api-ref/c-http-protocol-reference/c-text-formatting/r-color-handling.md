---
description: RTF规范允许使用\colortbl指定的RGB颜色值。 每个组件都分别提供了\red、\green和\blue命令。
seo-description: RTF规范允许使用\colortbl指定的RGB颜色值。 每个组件都分别提供了\red、\green和\blue命令。
seo-title: 颜色处理
solution: Experience Manager
title: 颜色处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6c51d204-27ca-4fbd-a297-bf1d04b63a3f
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 颜色处理{#color-handling}

RTF规范允许使用\colortbl指定的RGB颜色值。 每个组件都分别提供了\red、\green和\blue命令。

专有的RTF扩展命令 `\cmykcolortbl` 允许指定CMYK颜色，每个颜色组件都 `\cyan`提供 `\magenta`、 `\yellow`和 `\black` 命令。

的颜色组 `\colortbl` 件值在0到255之间。 的组件 `\cmykcolortbl` 值在0到100之间。

RTF extension命令 `\*\iscolortbl`由支持， `textPs=`它提供了一种指定带有标准图像服务颜色值的颜色表的方法，该颜色表完全支持RGB、灰色、CMYK和alpha。 它的语法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一个或多个IS颜色值，用&#39;;&#39;分隔

可以在同一或RTF字符串中指定多种类型 `text=` 的颜 `textPs=` 色表。 每个颜色表可以有不同数量的条目。 图像服务将尝试按以下顺序查找颜色：之 `\iscolortbl` 前( `\cmykcolortbl` 仅当文本图层的像素类型为CMYK时) `\colortbl`。 仅 `textPs=` 在需要时，颜色在CMYK和RGB之间精确转换（例如，指定RGB颜色但需要CMYK输出时）。 如果未找到特定索引值的颜色，则使用默认颜色（黑色）。

有关 [IS颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) （IS颜色值）语法的说明，请参阅color。

## Restrictions {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支持 `\*\iscolortbl`。 `textPs=` 不支持 `\cmykcolortbl`。

渲染Photofonts时忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，但在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
