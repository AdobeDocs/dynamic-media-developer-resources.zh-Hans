---
description: 模板可用于减少复合多个图像层或包含RTF格式文本的请求的长度和复杂性。
solution: Experience Manager
title: 模板
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 0%

---

# 模板{#templates}

模板可用于减少复合多个图像层或包含RTF格式文本的请求的长度和复杂性。

自定义变量可用于进一步简化模板的使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，模板主体位于`catalog::Modifier`字段中，而`catalog::Path`字段为空，或者指定不能动态更改的静态背景图像。

使用`template=`命令或请求URL的路径组件中指定了模板。 对于大多数应用程序，建议使用`template=`命令指定模板。 `template=`命令不得出现在`catalog::PostModifier`字段中，而只能出现在嵌套IS请求的`catalog::Modifier`字段中（即，在`src=is{...}`结构中）。 在`src=`或`mask=`命令中不能引用模板记录。

模板中嵌入的任何`src=`或`mask=`命令都可以解析到请求的主目录或其他图像目录。 如果未明确指定`rootId`，则假定为主目录。 使用`template=`指定的模板也可以位于主目录或其他图像目录中。

强烈建议始终包含模板中所用所有变量的默认定义。 这样，模板的图像输出总是可以通过指定其`attribute::RootId`和`catalog::Id`来查看，而无需知道模板中使用了哪些变量。

预定义路径替换变量`$object$`可用于将url路径中指定的图像对象应用到任何层源或蒙版（`src=`或`mask=`），即使在嵌套或嵌入的请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
