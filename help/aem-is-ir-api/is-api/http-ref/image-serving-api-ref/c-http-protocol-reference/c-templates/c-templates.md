---
description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-description: 模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。
seo-title: 模板
solution: Experience Manager
title: 模板
uuid: 54830d1f-40ad-4bf2-8e3d-d3e4d4ab57b9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 0%

---


# 模板{#templates}

模板可用于减少复合多个图像层或包括RTF格式文本的请求的长度和复杂性。

可使用自定义变量进一步简化模板的使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，模板正文位于`catalog::Modifier`字段中，而`catalog::Path`字段为空或指定了无法动态更改的静态背景图像。

模板是使用`template=`命令或在请求URL的路径组件中指定的。 对于大多数应用程序，建议使用`template=`命令指定模板。 `template=`命令不能出现在`catalog::PostModifier`字段中，而只能出现在嵌套IS请求（即在`src=is{...}`构造中）的`catalog::Modifier`字段中。 在`src=`或`mask=`命令中不能引用模板记录。

嵌入模板中的任何`src=`或`mask=`命令都可解析到请求的主目录或其他图像目录。 如果未显式指定`rootId`，则假定主目录。 使用`template=`指定的模板也可以位于主目录或其他图像目录中。

强烈建议始终包含模板中使用的所有变量的默认定义。 这样，模板的图像输出总是可以通过指定其`attribute::RootId`和`catalog::Id`来查看，而不必知道模板中使用了哪些变量。

预定义的路径替换变量`$object$`可用于将url路径中指定的图像对象应用到任何图层源或蒙版（`src=`或`mask=`），即使在嵌套或嵌入的请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
