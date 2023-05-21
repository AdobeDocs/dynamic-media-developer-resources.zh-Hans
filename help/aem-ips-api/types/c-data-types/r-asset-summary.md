---
description: 包含資產相關摘要資訊的中繼資料搜尋結果。
solution: Experience Manager
title: 資產摘要
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

包含資產相關摘要資訊的中繼資料搜尋結果。

语法

## 参数 {#section-ebc75cc024d94c439260d2e71873cc74}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 資產控點。 |
| 类型 | `xsd:string` | 资源类型. 「資產型別」常數會定義可能的值。 可选. |
| 名称 | `xsd:string` | 資產名稱。 可选. |
| 文件夹 | `xsd:string` | 包含資產的資料夾。 |
| 文件名 | `xsd:string` | 資產的檔案名稱。 |
| 已创建 | `xsd:dateTime` | 資產建立日期。 |
| createUser | `xsd:string` | 建立資產的使用者。 |
| lastModified | `xsd:dateTime` | 上次更新資產的日期。 |
| lastModifyUser | `xsd:string` | 上次修改資產的使用者。 |
| metadataArray | `types:MetadataArray` | 與資產相關聯的中繼資料值陣列。 |
| 分数 | `xsd:double` | 定義相似性搜尋時的精確度（0 =無相符專案，1 =完全相符）。 |
| scoredetail | `xsd:string` | 在相似性搜尋的結果中保留有關類似區域的詳細資訊。 |
