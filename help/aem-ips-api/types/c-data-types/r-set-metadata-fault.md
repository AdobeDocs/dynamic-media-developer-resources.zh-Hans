---
description: batchSetAssetMetadata操作中单个更新的警告或错误详细信息。
seo-description: batchSetAssetMetadata操作中单个更新的警告或错误详细信息。
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Dynamic Media Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---


# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中单个更新的警告或错误详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 元数据设置失败的资产。 |
| `*`fieldHandle`*` | `xsd:string` | 元数据字段的句柄，其值设置失败。 |
| `*`代码`*` | `xsd:int` | 错误代码。 |
| `*`原因`*` | `xsd:string` | 错误描述（纯文本）。 |

