---
description: 資產或資料夾的磁碟空間統計資料。
solution: Experience Manager
title: 磁碟使用量
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 14%

---

# [!DNL DiskUsage]{#diskusage}

資產或資料夾的磁碟空間統計資料。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司控點。 |
| companyName | `xsd:string` | 公司名称. |
| imageCount | `xsd:int` | 儲存的影像數目。 |
| diskSpaceUse | `xsd:long` | 檔案端總計（以KB為單位）。 |
| lastModified | `xsd:dateTime` | 日期、時間和時區 `DiskUsage` 上次修改型別。 |
