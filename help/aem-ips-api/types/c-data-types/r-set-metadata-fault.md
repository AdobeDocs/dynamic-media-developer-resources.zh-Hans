---
description: batchSetAssetMetadata操作中的新更新的警告或错误详细信息。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---

# SetMetadataFault{#setmetadatafault}

batchSetAssetMetadata操作中的新更新的警告或错误详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 元数据设置失败的资产。 |
| fieldHandle | `xsd:string` | 其值设置失败的元数据字段的句柄。 |
| 代码 | `xsd:int` | 故障代码。 |
| 原因 | `xsd:string` | 错误描述（纯文本）。 |
