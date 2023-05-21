---
description: PDF檔案選項。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF檔案選項。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 进度 | `xsd:string` | 選擇「PDF流程」。 |
| 解析度 | `xsd:double` | 檔案解析度。 |
| 色域 | `xsd:string` | 後置指令碼色彩空間模式選擇。 |
| pdfCatalog | `xsd:boolean` | 轉譯後是否要將多頁PDF合併到eCatalog （預設為true）。 |
| extractSearchWords | `xsd:boolean` | 是否要從PDF檔案擷取搜尋字詞。 |
| extractLinks | `xsd:boolean` | 是否將PDF連結擷取至指派給IPS內點陣化頁面的影像地圖。 |
