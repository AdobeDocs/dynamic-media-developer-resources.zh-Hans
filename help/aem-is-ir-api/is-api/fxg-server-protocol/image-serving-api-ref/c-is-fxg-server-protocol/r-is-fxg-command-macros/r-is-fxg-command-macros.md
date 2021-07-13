---
description: 命令宏为命令集提供了命名的快捷键。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏为命令集提供了命名的快捷键。

宏在单独的宏定义文件中定义，这些文件可附加到图像目录或默认目录。

可以在“？”之后的请求中的任意位置以及`catalog::Modifier`字段中的任意位置调用宏。 宏只能表示一个或多个完整的图像提供命令，因此必须由“&amp;”分隔符括起来（修饰符字符串的开头或结尾处除外）。

在解析期间，宏调用会被其替换字符串提前替换。 如果宏中的命令在请求中的宏调用之前发生，则它们将覆盖请求中的相同命令。 这与`catalog::Modifier`不同，在中，请求字符串中的命令将始终覆盖`catalog::Modifier`字符串中的命令，而不管请求中的位置如何。

可以嵌套宏，但存在以下限制：只有在分析宏定义时已经定义宏时，才能调用该宏，方法是先在同一宏定义文件中出现，或者将此类嵌入宏的定义置于默认宏定义文件中。

如果将相同的属性应用于不同的图像，则宏会非常有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我们可以为常用属性定义一个宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的使用方式如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

由于第三个请求的`wid=`不同，因此我们只需在调用宏的&#x200B;*之后覆盖值*（在&#x200B;*`$view$`之前指定`wid=`*&#x200B;将不会产生任何影响）。

+ [name](r-name.md)
