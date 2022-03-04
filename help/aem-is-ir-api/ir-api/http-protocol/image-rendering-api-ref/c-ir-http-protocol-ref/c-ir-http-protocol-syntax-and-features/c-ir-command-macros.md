---
title: 命令宏
description: 命令宏为命令集提供了命名的快捷键。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---

# 命令宏{#command-macros}

命令宏为命令集提供了命名的快捷键。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名称

宏在单独的宏定义文件中定义，可附加到材料目录或缺省目录。

*[!DNL name]* 不区分大小写，可由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成 字符.

在“？”之后的请求中的任意位置或在 `vignette::Modifier` 字段。 宏只能表示一个或多个“图像渲染”命令，并且必须与具有“&amp;”分隔符的其他命令分开。

在解析期间，宏调用会被其替换字符串提前替换。 如果宏中的命令在请求中的宏调用之前发生，则它们会覆盖请求中的相同命令。 此工作流与 `vignette::Modifier`，其中请求字符串中的命令会覆盖 `vignette::Modifier` 字符串，而不考虑请求中的位置。

命令宏不能具有参数值，但可以使用自定义变量将值从请求传递到宏。

不能嵌套宏。

**示例**

如果将相同的命令或属性应用于不同的渲染图像，则宏非常有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以为常用属性定义宏：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

因为 `qlt=` 对于第三个请求而言，不同的是，在调用宏后，软件会覆盖该值(指定 `qlt=` *之前* `$render$`无效)。

**另请参阅**

`catalog::MacroFile`, `catalog::Modifier`，宏定义参考

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
