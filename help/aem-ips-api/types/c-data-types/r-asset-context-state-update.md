---
title: AssetContextStateUpdate
description: 為與資產關聯的發佈內容設定一組新的發佈狀態旗標。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

為與資產關聯的發佈內容設定一組新的發佈狀態旗標。

**参数**

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 處理您要更新的資產。 |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 您要更新之資產的發佈聯絡狀態陣列。 |
