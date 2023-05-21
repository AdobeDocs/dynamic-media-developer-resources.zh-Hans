---
description: PostScript檔案選項。
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

PostScript檔案選項。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 进度 | `xsd:string` | PostScript程式選擇。 |
| 解析度 | `xsd:double` | 檔案解析度。 |
| 色域 | `xsd:string` | PostScript色彩空間模式。 |
| alpha | `xsd:boolean` | 是否將檔案點陣化成影像。 如果是這樣，如果以這種方式定義原始檔案，則會建立透明背景。 通常用於建立重疊圖志。 |
| extractSearchWords | `xsd:boolean` | 是否要從PostScript檔案擷取搜尋字詞。 |
