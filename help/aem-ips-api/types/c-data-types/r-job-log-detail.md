---
description: 工作記錄檔資訊。
solution: Experience Manager
title: 工作記錄詳細資訊
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

工作記錄檔資訊。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| logMessage | `xsd:string` | 工作記錄檔中的訊息。 |
| logType | `xsd:string` | 工作記錄檔型別。 |
| assetName | `xsd:string` | 工作記錄檔中的資產名稱（選擇性）。 |
| assetType | `xsd:string` | 資產型別的選擇。 |
| assetHandle | `xsd:string` | 工作記錄檔中參照的資產控制代碼。 |
| auxArray | `types:JobLogDetailAuxArray` | 提供上述五種工作記錄型別以外的其他詳細工作記錄資訊。 |
