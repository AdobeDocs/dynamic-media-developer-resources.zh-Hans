---
description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-title: 模板
solution: Experience Manager
title: 模板
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---


# 模板{#templates}

模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。

可使用自定义变量进一步简化模板使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，`catalog::Modifier`字段中的模板正文为空，或者指定无法动态更改的静态背景图像。`catalog::Path`

模板是使用`template=`命令或在请求URL的路径组件中指定的。 对于大多数应用程序，建议使用`template=`命令指定模板。 `template=`命令不能出现在`catalog::PostModifier`字段中，并且只能出现在嵌套IS请求（即在`src=is{...}`构造中）的`catalog::Modifier`字段中。 模板记录不能在`src=`或`mask=`命令中引用。

嵌入模板中的任何`src=`或`mask=`命令都可解析到请求的主目录或其他图像目录。 如果未明确指定`rootId`，则假定主目录。 使用`template=`指定的模板也可能位于主目录或其他图像目录中。

强烈建议始终包含模板中使用的所有变量的默认定义。 这样，只需指定模板的`attribute::RootId`和`catalog::Id`即可查看模板的图像输出，无需知道模板中使用了哪些变量。

预定义的路径替换变量`$object$`可用于将url路径中指定的图像对象应用到任何图层源或蒙版（`src=`或`mask=`），即使在嵌套或嵌入的请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
