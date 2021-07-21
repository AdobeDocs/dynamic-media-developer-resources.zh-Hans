---
description: PDF文件选项。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 9%

---

# PDFOptions{#pdfoptions}

PDF文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`进度`*` | `xsd:string` | 选择“PDF流程”。 |
| `*`resolution`*` | `xsd:double` | 文件解析。 |
| `*`颜色空间`*` | `xsd:string` | 后脚本Colorspace模式选择。 |
| `*`pdfCatalog`*` | `xsd:boolean` | 呈现后是否将多页面PDF合并到eCatalog中（默认值为true）。 |
| `*`extractSearchWords`*` | `xsd:boolean` | 是否从PDF文件中提取搜索词。 |
| `*`extractLinks`*` | `xsd:boolean` | 是否将PDF链接提取到IPS中分配给光栅化页面的图像映射中。 |
