---
title: 模板
description: 模板可用于减少复合多个图像层或包含RTF格式文本的请求的长度和复杂性。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef49cf8a-4621-4114-aae5-5178f6a5160d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# 模板{#templates}

模板可用于减少复合多个图像层或包含RTF格式文本的请求的长度和复杂性。

自定义变量可用于进一步简化模板的使用。 模板通常设置为允许轻松交换图像或文本，或在运行时设置其他选项。

模板作为记录存储在图像目录中，模板正文位于 `catalog::Modifier` 字段，以及 `catalog::Path` 字段为空或指定不能动态更改的静态背景图像。

模板由 `template=` 命令或请求URL的路径组件中。 对于大多数应用程序，建议使用 `template=` 命令来指定模板。 的 `template=`命令不得出现在 `catalog::PostModifier` 字段，并且只能出现在 `catalog::Modifier` 字段(例如， `src=is{...}` 构造)。 模板记录可能未在 `src=` 或 `mask=`中。

任意 `src=` 或 `mask=`嵌入在模板中的命令可以解析到请求的主目录或到不同的图像目录。 如果否 `rootId` 显式指定，则假定是主目录。 指定的模板 `template=` 也可能位于主目录或其他图像目录中。

强烈建议始终包含模板中所用所有变量的默认定义。 这样，模板的图像输出总是可以通过指定其 `attribute::RootId` 和 `catalog::Id`，而无需知道模板中使用的变量。

预定义路径替换变量 `$object$` 可用于将url路径中指定的图像对象应用到任何层源或蒙版( `src=` 或 `mask=`)，即使在嵌套或嵌入的请求中也是如此。

* [示例A](r-example-a.md)
* [示例B](r-example-b.md)
* [示例C](r-example-c.md)
