---
description: 命令宏为命令集提供命名的快捷键。
seo-description: 命令宏为命令集提供命名的快捷键。
seo-title: 命令宏
solution: Experience Manager
title: 命令宏
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b

---


# 命令宏{#command-macros}

命令宏为命令集提供命名的快捷键。

宏在单独的宏定义文件中定义，这些文件可以附加到图像目录或默认目录。

宏可以在“?”之后的请求中的任意位置以及字段中的任意位 `catalog::Modifier` 置调用。 宏只能表示一个或多个完整的图像服务命令，因此必须用“&amp;”分隔符（修饰符字符串的开头或结尾处除外）来包围。

在解析过程中，宏调用会被替换为其替换字符串。 如果宏中的命令在请求中的宏调用之前发生，则它们将覆盖请求中的相同命令。 这与请求字符串 `catalog::Modifier`中的命令始终覆盖字符串中的命令不同，而 `catalog::Modifier` 不管请求中的位置如何。

宏可以嵌套，但有以下限制：只有在分析宏定义时已定义宏时，才能调用宏，方法是先在同一宏定义文件中显示，或将此类嵌入宏的定义放入默认宏定义文件中。

如果将相同的属性应用于不同的图像，则宏可能很有用。

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

我们可以为常见属性定义一个宏：

`view wid=240&fmt=pdf&imageRes=300`

宏的用法如下：

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

由于 `wid=` 第三个请求不同，我们只需在调用宏 *后* (指定 `wid=`*before *`$view$`不会产生任何效果)覆盖值。

+ [名称](r-name.md)
