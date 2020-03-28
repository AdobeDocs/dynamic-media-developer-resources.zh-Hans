---
description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-title: 模板
solution: Experience Manager
title: 模板
topic: Scene7 Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# 模板{#templates}

模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。

自定义变量可用于进一步简化模板的使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，而模板正文在字 `catalog::Modifier` 段中，且字段为空或指定了无法动态更改的 `catalog::Path` 静态背景图像。

模板是使用命令 `template=` 或请求URL的路径组件指定的。 对于大多数应用程序，建议使用 `template=` 命令指定模板。 该 `template=`命令不能出现在字段 `catalog::PostModifier` 中，并且只能出现在嵌套 `catalog::Modifier` IS请求（即在构造中）的字 `src=is{...}` 段中。 模板记录不能在或命令 `src=` 中引 `mask=`用。

嵌入 `src=` 在模 `mask=`板中的任何或命令都可能解析到请求的主目录或其他图像目录。 如果未显 `rootId` 式指定，则假定使用主目录。 使用指定的模 `template=` 板也可能位于主目录或其他图像目录中。

强烈建议始终包含模板中使用的所有变量的默认定义。 这样，只需指定模板的图像输出，即可始终查看模板的图像输 `attribute::RootId` 出 `catalog::Id`，而不必知道模板中使用了哪些变量。

预定义的路径替 `$object$` 换变量可用于将url路径中指定的图像对象应用到任何图层源或蒙版(或 `src=``mask=`)，即使在嵌套或嵌入的请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
