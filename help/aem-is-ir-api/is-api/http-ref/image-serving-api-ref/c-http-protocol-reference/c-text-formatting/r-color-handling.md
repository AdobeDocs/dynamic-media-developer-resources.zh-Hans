---
description: RTF规范允许使用&bsol；colortbl指定的RGB颜色值。 每个组件都单独提供了&bsol；red、&bsol；green和&bsol；blue命令。
solution: Experience Manager
title: 颜色处理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 颜色处理{#color-handling}

RTF规范允许使用指定的RGB颜色值 `\colortbl`. 每个组件分别配备有 `\red`， `\green`、和 `\blue` 命令。

专有RTF扩展命令 `\cmykcolortbl` 允许指定CMYK颜色，每个颜色组件都随附有 `\cyan`， `\magenta`， `\yellow`、和 `\black` 命令。

颜色组件值 `\colortbl` 在0到255之间。 的组件值 `\cmykcolortbl` 在0到100之间。

RTF扩展命令 `\*\iscolortbl`，支持 `textPs=`，提供了一种使用标准“图像服务”颜色值指定颜色表的方法，该方法支持全RGB、灰度、CMYK和Alpha。 其语法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一个或多个IS颜色值，以“；”分隔

可以在同一颜色表中指定多种类型的颜色表 `text=` 或 `textPs=` rtf字符串。 每个颜色表可以有不同的条目数。 图像服务将尝试按以下顺序查找颜色： `\iscolortbl` 早于 `\cmykcolortbl` （仅当文本图层的像素类型为CMYK时） `\colortbl`. 对象 `textPs=` 仅在需要时(例如，指定RGB颜色但需要CMYK输出时)，才能在CMYK和RGB之间准确转换颜色。 如果找不到特定索引值的颜色，则使用默认颜色（黑色）。

请参阅 [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 有关IS颜色值的语法的说明。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

`text=` 不支持 `\*\iscolortbl`. `textPs=` 不支持 `\cmykcolortbl`.

渲染Photofonts时忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
