---
description: 图像渲染源数据文件包括晕影文件、材质文件（用于可重复纹理和标记的图像，以及文件柜和窗口覆盖样式文件）和ICC配置文件。
solution: Experience Manager
title: 源数据
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---

# 源数据{#source-data}

图像渲染源数据文件包括晕影文件、材质文件（用于可重复纹理和标记的图像，以及文件柜和窗口覆盖样式文件）和ICC配置文件。

所有源数据文件都必须可供图像渲染的本机代码组件访问（与图像服务器共存）。

如果涉及材料目录，则在材料目录中指定的文件(带有 `vignette::Path`， `catalog::Path`，或 `icc::ProfilePath`)将由渲染服务器查找，如下所示：

* 如果路径是绝对路径，则按原样使用。
* 如果路径是相对路径，则会添加前缀 `catalog::RootPath` （来自已命名的材料目录）。
* 如果路径是绝对路径，则使用它；否则，将使用前缀 `default::RootPath` （从默认目录中）。
* 如果路径为绝对路径，则使用该路径；否则，服务器会将其与中指定的路径合并 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* 如果路径现在为绝对路径，则使用该路径；否则，将假定该路径相对于[！DNL  *[!DNL install_folder]*]。

如果未涉及图像目录，则路径将与 `default::RootPath` 然后按上述方法处理。

通常使用指定源数据文件的物理位置 [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). 可以指定多个值以允许源数据文件跨多个文件系统分发。 渲染服务器将按指定的顺序尝试每个路径，直到找到数据文件为止。

可以随时添加任何类型的新数据文件，而无需停止服务器。
