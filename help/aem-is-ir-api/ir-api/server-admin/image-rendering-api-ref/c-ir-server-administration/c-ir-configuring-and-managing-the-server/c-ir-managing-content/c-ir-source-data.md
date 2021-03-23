---
description: “图像渲染”源数据文件包括晕影文件、材料文件（用于可重复纹理和倾斜的图像，以及包含样式文件的机柜和窗口）和ICC用户档案。
seo-description: “图像渲染”源数据文件包括晕影文件、材料文件（用于可重复纹理和倾斜的图像，以及包含样式文件的机柜和窗口）和ICC用户档案。
seo-title: 源数据
solution: Experience Manager
title: 源数据
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员，业务从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---


# 源数据{#source-data}

“图像渲染”源数据文件包括晕影文件、材料文件（用于可重复纹理和倾斜的图像，以及包含样式文件的机柜和窗口）和ICC用户档案。

所有源数据文件都必须可由图像渲染的本机代码组件访问（与图像服务器共同位置）。

如果涉及材料目录，则渲染服务器将查找在材料目录（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的文件，如下所示：

* 如果路径为绝对路径，则按原样使用。
* 如果路径为相对路径，则其前缀为`catalog::RootPath`（来自命名材料目录）。
* 如果路径为绝对路径，则使用它；否则，它前缀为`default::RootPath`（来自默认目录）。
* 如果路径为绝对路径，则使用它；否则，服务器会将其与在[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路径组合在一起。
* 如果路径现在为绝对路径，则使用它；否则，假定它是相对于[!DNL *[!DNL install_folder]*]的。

如果未涉及图像目录，则路径将与`default::RootPath`组合，然后按上述方式处理。

源数据文件的物理位置通常使用[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多个值以允许在多个文件系统中分发源数据文件。 渲染服务器将按指定的顺序尝试每个路径，直到找到数据文件。

可以随时添加任何类型的新数据文件，而无需停止服务器。
