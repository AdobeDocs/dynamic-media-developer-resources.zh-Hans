---
description: PDF文件选项。
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 9%

---


# PDFOptions{#pdfoptions}

PDF文件选项。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`进度`*` | `xsd:string` | 选择“PDF流程”。 |
| `*`分辨率`*` | `xsd:double` | 文件分辨率。 |
| `*`颜色空间`*` | `xsd:string` | “后脚本色彩空间模式”选项。 |
| `*`pdfCatalog`*` | `xsd:boolean` | 渲染后是否将多页PDF合并到电子目录中（默认为true）。 |
| `*`extractSearchWords`*` | `xsd:boolean` | 是否从PDF文件中提取搜索词。 |
| `*`extractLinks`*` | `xsd:boolean` | 是否将PDF链接提取到指定给IPS中栅格化页面的图像映射中。 |

