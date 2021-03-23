---
description: 命令宏为命令集提供命名的快捷键。
seo-description: 命令宏为命令集提供命名的快捷键。
seo-title: 命令宏*
solution: Experience Manager
title: 命令宏*
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 1%

---


# 命令宏*{#command-macros}

命令宏为命令集提供命名的快捷键。

`$ *[!DNL name]*$`

** *[!DNL name]* **宏名称

宏在单独的宏定义文件中定义，可以附加到材料目录或默认目录。

*[!DNL name]* 不区分大小写，并且可以由ASCII字母、数字、“ — ”、“_”和“。”的任意组合组成字符.

在“？”之后或`vignette::Modifier`字段内的任意位置调用请求中的宏。 宏只能表示一个或多个完整的图像渲染命令，并且必须与具有“&amp;”分隔符的其他命令分开。

在分析的早期，宏调用会被替换字符串替换。 如果宏中的命令在请求中调用宏之前发生，则它们会覆盖请求中的相同命令。 这与`vignette::Modifier`不同，其中请求字符串中的命令始终会覆盖`vignette::Modifier`字符串中的命令，而与请求中的位置无关。

命令宏不能有参数值，但可以使用自定义变量将值从请求传递到宏。

宏可能未嵌套。

**示例**

如果将相同的命令或属性应用于不同的渲染图像，则宏可能很有用。

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

您可以为通用属性定义宏：

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

宏的用法如下：

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

由于第三个请求的`qlt=`不同，因此我们只在调用宏后覆盖该值（在&#x200B;*`$render$`之前指定`qlt=`*&#x200B;将不会产生任何效果）。

**另请参阅**

`catalog::MacroFile`、, `catalog::Modifier`宏定义参考

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

