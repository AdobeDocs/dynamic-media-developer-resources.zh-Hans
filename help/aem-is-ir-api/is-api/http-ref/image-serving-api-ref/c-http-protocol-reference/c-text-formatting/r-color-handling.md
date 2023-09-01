---
title: 颜色处理
description: RTF规范允许使用&bsol；colortbl指定的RGB颜色值。 每个组件分别提供了&bsol；red、&bsol；green和&bsol；blue命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# 颜色处理{#color-handling}

RTF规范允许使用指定的RGB颜色值 `\colortbl`. 每个组件分别设置 `\red`， `\green`、和 `\blue` 命令。

专有RTF扩展命令 `\cmykcolortbl` 允许指定CMYK颜色，每个颜色组件都随 `\cyan`， `\magenta`， `\yellow`、和 `\black` 命令。

颜色组件值 `\colortbl` 在0到255之间。 的组件值 `\cmykcolortbl` 在0到100之间。

RTF扩展命令 `\*\iscolortbl`，由支持 `textPs=`，提供了一种通过标准图像服务颜色值指定色表的方法，该方法支持全RGB、灰度、CMYK和Alpha。 它具有以下语法：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]* 一个或多个IS颜色值，以“；”分隔

可以在同一颜色表中指定多种类型的颜色表 `text=` 或 `textPs=` rtf字符串。 每个颜色表可以有不同的条目数。 图像服务尝试按以下顺序查找颜色： `\iscolortbl` 早于 `\cmykcolortbl` （仅当文本图层的像素类型为CMYK时）之前 `\colortbl`. 对象 `textPs=` 仅在需要时才能在CMYK和RGB之间精确转换(例如，当指定了RGB但需要CMYK输出时)。 如果找不到特定索引值的颜色，则使用默认颜色（黑色）。

请参阅 [颜色](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) 有关IS颜色值的语法的说明。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修饰符 `text=` 不支持 `\*\iscolortbl`. 修饰符 `textPs=` 不支持 `\cmykcolortbl`.

渲染Photofonts时将忽略颜色选择。

## 示例 {#section-0f166bb72bd44479be01131077851142}

允许使用变量控制三种文本颜色，同时当在标准RTF文本编辑器中打开RTF字符串时仍显示颜色默认值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
