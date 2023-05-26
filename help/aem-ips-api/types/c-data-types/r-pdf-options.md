---
description: 文件选项PDF。
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

文件选项PDF。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 进度 | `xsd:string` | 选择“PDF流程”。 |
| 解析度 | `xsd:double` | 文件解析。 |
| 颜色空间 | `xsd:string` | 后脚本色彩空间模式选项。 |
| pdfCatalog | `xsd:boolean` | 是否在呈现后将多页PDF合并到eCatalog中（默认值为true）。 |
| extractSearchWords | `xsd:boolean` | 是否从PDF文件中提取搜索词。 |
| extractLinks | `xsd:boolean` | 是否将PDF链接提取到分配给IPS内栅格化页面的图像映射中。 |
