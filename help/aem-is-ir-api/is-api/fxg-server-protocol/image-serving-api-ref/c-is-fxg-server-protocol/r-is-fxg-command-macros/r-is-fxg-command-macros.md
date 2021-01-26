---
description: 命令宏为命令集提供命名的快捷键。
seo-description: 命令宏为命令集提供命名的快捷键。
seo-title: 命令宏
solution: Experience Manager
title: 命令宏
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# 命令宏{#command-macros}

命令宏为命令集提供命名的快捷键。

宏在单独的宏定义文件中定义，可以附加到图像目录或默认目录。

可以在“?”之后的请求中的任意位置以及`catalog::Modifier`字段中的任意位置调用宏。 宏只能表示一个或多个完整的图像服务命令，因此必须用“&amp;”分隔符（修饰符字符串的开头或结尾处除外）来封装。

在分析的早期，宏调用被其替换字符串替换。 如果宏中的命令在请求中调用宏之前发生，则它们将覆盖请求中的相同命令。 这与`catalog::Modifier`不同，其中请求字符串中的命令始终会覆盖`catalog::Modifier`字符串中的命令，而不管请求中的位置如何。

宏可以嵌套，但有以下限制：只有在分析宏定义时已定义宏时，才能调用宏，方法是显示在同一宏定义文件中的较早位置，或者将此类嵌入宏的定义放置到默认宏定义文件中。

如果将同一属性应用于不同的图像，则宏可能很有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我们可以为通用属性定义一个宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的用法如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

由于第三个请求的`wid=`不同，我们只需在调用宏&#x200B;*后覆盖值*（在&#x200B;*`$view$`前指定`wid=`*&#x200B;将不会产生任何效果）。

+ [name](r-name.md)
