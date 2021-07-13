---
description: 命令宏为命令集提供了命名的快捷键。
solution: Experience Manager
title: 命令宏*
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 1%

---

# 命令宏*{#command-macros}

命令宏为命令集提供了命名的快捷键。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名称

宏在单独的宏定义文件中定义，可附加到材料目录或缺省目录。

*[!DNL name]* 不区分大小写，可由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成字符.

在“？”之后的请求中的任意位置或`vignette::Modifier`字段中的任意位置调用宏。 宏只能表示一个或多个完整的“图像渲染”命令，并且必须与具有“&amp;”分隔符的其他命令分开。

在解析期间，宏调用会被其替换字符串提前替换。 如果宏中的命令在请求中的宏调用之前发生，则它们会覆盖请求中的相同命令。 这与`vignette::Modifier`不同，在中，请求字符串中的命令将始终覆盖`vignette::Modifier`字符串中的命令，而不管请求中的位置如何。

命令宏不能具有参数值，但可以使用自定义变量将值从请求传递到宏。

不能嵌套宏。

**示例**

如果将相同的命令或属性应用于不同的渲染图像，则宏非常有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以为常用属性定义宏：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的使用方式如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

由于第三个请求的`qlt=`不同，因此我们只需在调用宏后覆盖值（在&#x200B;*`$render$`之前指定`qlt=`*&#x200B;将不会产生任何效果）。

**另请参阅**

`catalog::MacroFile`、, `catalog::Modifier`宏定义引用

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
