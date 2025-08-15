---
title: 命令宏
description: 命令宏为命令集提供命名快捷键。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# 命令宏{#command-macros}

命令宏为命令集提供命名快捷键。

宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。

宏可以在“？”之后的请求中任意位置调用，也可以在`catalog::Modifier`字段中的任何位置调用。 宏只能表示一个或多个完整的图像提供命令，因此必须用“&amp;”分隔符括起来（修饰符字符串的开头或结尾处除外）。

在解析过程中，宏调用在早期被替换字符串替换。 如果宏中的命令发生在请求中的宏调用之前，则宏中的命令会覆盖请求中的相同命令。 此流程不同于`catalog::Modifier`，在这种情况下，无论请求中的位置如何，请求字符串中的命令始终会覆盖`catalog::Modifier`字符串中的命令。

宏可以嵌套。 但是，只有在宏定义被解析时已定义时，才能调用该宏。 此流程可通过以下方法完成：先在同一宏定义文件中显示，或将此类嵌入宏的定义置于缺省宏定义文件中。

如果将相同的属性应用到不同的图像，则宏会很有用。

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

您可以为公共属性定义宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的使用方式如下：

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

由于第三个请求的`wid=`不同，您只需在&#x200B;*之后覆盖值*&#x200B;即可调用宏（在`wid=` *之前指定* `$view$`无效）。

+ [名称](r-name.md)
