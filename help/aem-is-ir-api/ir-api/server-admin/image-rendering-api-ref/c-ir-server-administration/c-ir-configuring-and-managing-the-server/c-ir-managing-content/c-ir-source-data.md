---
description: 图像渲染源数据文件包括暗角文件、材料文件（可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。
seo-description: 图像渲染源数据文件包括暗角文件、材料文件（可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。
seo-title: 源数据
solution: Experience Manager
title: 源数据
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# 源数据{#source-data}

图像渲染源数据文件包括暗角文件、材料文件（可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。

所有源数据文件必须可由图像渲染的本机代码组件访问（与图像服务器共同位置）。

如果涉及材料目录，Render Server会按如下方式查找在材料目录（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的文件：

* 如果路径为绝对路径，则按原样使用。
* 如果路径为相对路径，则其前缀为`catalog::RootPath`（来自命名材料目录）。
* 如果路径为绝对路径，则使用它；否则，它前缀为`default::RootPath`（从默认目录）。
* 如果路径为绝对路径，则使用它；否则，服务器将其与[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路径相结合。
* 如果路径现在为绝对路径，则使用它；否则，假定它是相对于[!DNL *[!DNL install_folder]*]的。

如果未涉及图像目录，则路径将与`default::RootPath`组合，然后按上述方式处理。

源数据文件的物理位置通常使用[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多个值以允许在多个文件系统中分发源数据文件。 渲染服务器将按指定的顺序尝试每个路径，直到找到数据文件。

可以随时添加任何类型的新数据文件，而无需停止服务器。
