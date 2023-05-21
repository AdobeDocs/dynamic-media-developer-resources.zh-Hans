---
description: 屬於影像集的資產。
solution: Experience Manager
title: 影像整合員
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

屬於影像集的資產。

頁面重設表示 [!DNL eCatalog] 應該會開始一個新頁面。 `RenderSet` 表示它屬於 `RenderSet` 色票。 值會強製為 `true` 的 `eCatalog` 和 `RenderSet` 集。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| asset | `type:Asset` | 影像集陣列中的資產。 |
| pageReset | `xsd:boolean` | 開始新頁面。 會忽略設定，且值會強製為 `true` 的 `eCatalog` 和 `RenderSet` 集。 |
