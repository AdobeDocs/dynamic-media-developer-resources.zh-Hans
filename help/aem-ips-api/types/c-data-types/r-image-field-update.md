---
description: 更新與影像資產關聯的影像欄位。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

更新與影像資產關聯的影像欄位。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 資產控點。 |
| [!DNL resolution] | `xsd:double` | 影像解析度（畫素/英吋）。 |
| [!DNL anchorX] | `xsd:int` | X軸影像錨點。 |
| [!DNL anchorY] | `xsd:int` | Y軸影像錨點。 |
| [!DNL userData] | `xsd:string` | 值 `userData` 中繼資料欄位，已發佈至影像伺服使用者資料目錄欄位。 |
