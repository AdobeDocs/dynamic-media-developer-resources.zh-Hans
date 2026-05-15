---
description: PDF文件选项。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

PDF文件选项。

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
