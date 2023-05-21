---
description: PostScript檔案屬性。
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '45'
ht-degree: 11%

---

# [!DNL GenerationInfo]{#generationinfo}

PostScript檔案屬性。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| [!DNL engine] | `xsd:string` | 使用的產生引擎（請參閱「產生資訊」以瞭解值）。 |
| [!DNL originator] | `types:Asset` | 產生中使用的主要資產的資產記錄。 |
| [!DNL generated] | `types:Asset` | 所產生資產的資產記錄。 |
| 屬性陣列 | `types:GenerationAttributeArray` | 與產生程式相關聯的屬性陣列。 |
