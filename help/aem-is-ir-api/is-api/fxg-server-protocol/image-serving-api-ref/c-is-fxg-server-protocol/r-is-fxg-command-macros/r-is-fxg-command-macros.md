---
description: 命令宏为命令集提供命名快捷键。
solution: Experience Manager
title: 命令宏
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏为命令集提供命名快捷键。

宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。

可以在“？”之后的请求中的任何位置调用宏，也可以在 `catalog::Modifier` 字段。 宏只能表示一个或多个完整的图像提供命令，因此必须用“&amp;”分隔符括起来（修饰符字符串的开头或结尾处除外）。

在解析过程中，宏调用在早期被替换字符串替换。 如果宏中的命令发生在请求中的宏调用之前，则宏中的命令将覆盖请求中的相同命令。 这与不同 `catalog::Modifier`，其中请求字符串中的命令将始终覆盖 `catalog::Modifier` 字符串，而不考虑请求中的位置。

可以嵌套宏，但有下列限制：只有在宏定义解析时已定义宏时，才能调用该宏，方法是在同一宏定义文件中先显示宏，或者在缺省宏定义文件中放置此类嵌入宏的定义。

如果将相同的属性应用于不同的图像，则宏非常有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我们可以为公共属性定义宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的使用方式如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

从 `wid=` 对于第三个请求不同，我们只需覆盖值 *之后* 调用宏(指定 `wid=`*早于* `$view$` 不会产生任何效果)。

+ [名称](r-name.md)
