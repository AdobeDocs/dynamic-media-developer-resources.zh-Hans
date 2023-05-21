---
description: batchSetAssetMetadata作業中使用更新的警告或錯誤詳細資料。
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

batchSetAssetMetadata作業中使用更新的警告或錯誤詳細資料。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 中繼資料設定失敗的資產。 |
| fieldHandle | `xsd:string` | 設定值失敗的中繼資料欄位的控制代碼。 |
| 代码 | `xsd:int` | 錯誤碼。 |
| 原因 | `xsd:string` | 錯誤說明（純文字）。 |
