---
description: 图像渲染源数据文件包括晕影文件、材料文件（用于可重复纹理和标记的图像，以及文件柜和窗口覆盖样式文件）和ICC配置文件。
solution: Experience Manager
title: Source数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Source数据{#source-data}

图像渲染源数据文件包括晕影文件、材料文件（用于可重复纹理和标记的图像，以及文件柜和窗口覆盖样式文件）和ICC配置文件。

所有源数据文件都必须可供图像渲染的本机代码组件访问（与图像服务器位于同一位置）。

如果涉及材质目录，则渲染服务器将查找材质目录（包含`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的文件，如下所示：

* 如果路径是绝对路径，则按原样使用。
* 如果路径是相对路径，则以`catalog::RootPath`为前缀（来自命名材质目录）。
* 如果路径为绝对路径，则使用该路径；否则，该路径将以`default::RootPath`为前缀（来自默认目录）。
* 如果该路径为绝对路径，则使用该路径；否则，服务器会将其与[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路径合并。
* 如果路径现在为绝对路径，则使用该路径；否则，将假定该路径相对于[!DNL *[!DNL install_folder]*]。

如果未涉及图像目录，则路径将与`default::RootPath`组合在一起，然后按上述方式处理。

源数据文件的物理位置通常使用[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多个值以允许源数据文件跨多个文件系统分发。 渲染服务器按指定的顺序尝试每个路径，直到找到数据文件。

任何类型的新数据文件都可以随时添加，而无需停止服务器。
