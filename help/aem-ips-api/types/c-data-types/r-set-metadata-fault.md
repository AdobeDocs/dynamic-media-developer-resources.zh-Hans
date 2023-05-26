---
description: 在batchSetAssetMetadata操作中使用更新的警告或错误详细信息。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 12%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

在batchSetAssetMetadata操作中使用更新的警告或错误详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 其元数据设置失败的资源。 |
| fieldHandle | `xsd:string` | 设置值失败的元数据字段的句柄。 |
| 代码 | `xsd:int` | 错误代码。 |
| 原因 | `xsd:string` | 错误描述（纯文本）。 |
