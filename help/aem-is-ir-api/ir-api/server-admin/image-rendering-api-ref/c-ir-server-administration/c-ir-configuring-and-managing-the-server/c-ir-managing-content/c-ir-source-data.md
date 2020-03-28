---
description: 图像渲染源数据文件包括暗角文件、材料文件（用于可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。
seo-description: 图像渲染源数据文件包括暗角文件、材料文件（用于可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。
seo-title: 源数据
solution: Experience Manager
title: 源数据
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 源数据{#source-data}

图像渲染源数据文件包括暗角文件、材料文件（用于可重复纹理和装饰的图像，以及覆盖样式文件的机柜和窗口）和ICC用户档案。

所有源数据文件必须可由图像渲染的本机代码组件访问（与图像服务器共享）。

如果涉及材料目录，则Render Server会按如下方式查找在材料目录( `vignette::Path`with `catalog::Path`、 `icc::ProfilePath`or)中指定的文件：

* 如果路径为绝对路径，则按原样使用。
* 如果路径为相对路径，则其前缀为( `catalog::RootPath` 来自命名的材料目录)。
* 如果路径是绝对的，则使用它；否则，它的前缀 `default::RootPath` 为（从默认目录）。
* 如果路径是绝对的，则使用它；否则，服务器将其与ir.resourceRootPaths中指定的路 [径组合在一起](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。
* 如果路径现在是绝对的，则使用它；否则，假定它是相对于[!DNL *[!DNL install_folder]*]的。

如果不涉及图像目录，则路径将与之组合， `default::RootPath` 然后按上述方式处理。

源数据文件的物理位置通常使用 [ir.resourceRootPaths指定](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)。 可以指定多个值以允许源数据文件分布在多个文件系统中。 渲染服务器将按指定的顺序尝试每个路径，直到找到数据文件。

可以随时添加任何类型的新数据文件而无需停止服务器。
