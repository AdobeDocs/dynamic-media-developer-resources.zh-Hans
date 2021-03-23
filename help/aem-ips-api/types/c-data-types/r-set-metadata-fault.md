---
description: batchSetAssetMetadata操作中使用更新的警告或错误详细信息。
seo-description: batchSetAssetMetadata操作中使用更新的警告或错误详细信息。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中使用更新的警告或错误详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 元数据设置失败的资产。 |
| `*`fieldHandle`*` | `xsd:string` | 设置其值的元数据字段的句柄未成功。 |
| `*`代码`*` | `xsd:int` | 错误代码。 |
| `*`原因`*` | `xsd:string` | 错误描述（纯文本）。 |

