---
description: 图像渲染源数据文件包括晕影文件、材料文件（用于可重复纹理和标志的图像，以及覆盖样式文件的机柜和窗口）以及ICC配置文件。
solution: Experience Manager
title: 源数据
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# 源数据{#source-data}

图像渲染源数据文件包括晕影文件、材料文件（用于可重复纹理和标志的图像，以及覆盖样式文件的机柜和窗口）以及ICC配置文件。

所有源数据文件必须可由图像渲染的本机代码组件访问（与图像服务器共同位置）。

如果涉及材料目录，则渲染服务器将查找材料目录（具有`vignette::Path`、`catalog::Path`或`icc::ProfilePath`）中指定的文件，如下所示：

* 如果路径为绝对路径，则按原样使用。
* 如果路径为相对路径，则其前缀为`catalog::RootPath`（来自命名的材料目录）。
* 如果路径为绝对路径，则使用该路径；否则，其前缀为`default::RootPath`（从默认目录中）。
* 如果路径为绝对路径，则使用该路径；否则，服务器会将其与[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)中指定的路径组合在一起。
* 如果路径现在为绝对路径，则使用该路径；否则，它假定为相对于[!DNL *[!DNL install_folder]*]。

如果未涉及图像目录，则该路径将与`default::RootPath`组合，然后按照上述方式进行处理。

源数据文件的物理位置通常使用[ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2)指定。 可以指定多个值，以允许源数据文件跨多个文件系统分发。 呈现服务器将按指定的顺序尝试每个路径，直到找到数据文件为止。

任何类型的新数据文件都可以随时添加，而无需停止服务器。
