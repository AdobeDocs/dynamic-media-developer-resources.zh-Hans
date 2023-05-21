---
description: 從PDF檔案擷取的搜尋字串記錄。
solution: Experience Manager
title: SearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3f67ba8a-12dd-4698-9502-7cbdec9cb25d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# [!DNL SearchStrings]{#searchstrings}

從PDF檔案擷取的搜尋字串記錄。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| searchString | `xsd:string` | 搜尋字串文字。 |
| 關鍵字陣列 | `types:KeywordsArray` | 搜尋字串中的關鍵字陣列。 |
| 状态 | `xsd:boolean` | 如果搜尋字串有效且已啟用，則為True。 |
| x | `xsd:int` | 搜尋字串的X軸位置。 |
| y | `xsd:int` | 搜尋字串的Y軸位置。 |
| 宽度 | `xsd:int` | 搜尋字串寬度。 |
| 高度 | `xsd:int` | 搜尋字串高度。 |
| 字型名稱 | `xsd:string` | 搜尋字串中使用的字型名稱。 |
| pointSize | `xsd:string` | 字体大小. |
