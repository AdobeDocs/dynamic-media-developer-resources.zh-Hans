---
title: 模板
description: 模板可用于减少合成多个图像层或包括RTF格式文本的要求长度和复杂性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 模板{#templates}

模板可用于减少合成多个图像层或包括RTF格式文本的要求长度和复杂性。

自定义变量可用于进一步简化模板使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，模板正文位于`catalog::Modifier`字段中，`catalog::Path`字段为空，或者指定了无法动态更改的静态背景图像。

模板是通过`template=`命令或在请求URL的路径组件中指定的。 对于大多数应用程序，建议使用`template=`命令指定模板。 `template=`命令不能出现在`catalog::PostModifier`字段中，而且只能出现在嵌套IS请求（即`src=is{...}`构造）的`catalog::Modifier`字段中。 `src=`或`mask=`命令中可能未引用模板记录。

模板中嵌入的任何`src=`或`mask=`命令都可以解析为请求的主目录或不同的图像目录。 如果未显式指定`rootId`，则假定为主目录。 使用`template=`指定的模板也可能位于主目录或其他图像目录中。

强烈建议始终在模板中使用所有变量的默认定义。 这样，模板的图像输出始终可以通过指定其`attribute::RootId`和`catalog::Id`来查看，而无需知道模板中使用了哪些变量。

预定义的路径替换变量`$object$`可用于将URL路径中指定的图像对象应用到任何图层源或蒙版（`src=`或`mask=`），即使在嵌套或嵌入请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
