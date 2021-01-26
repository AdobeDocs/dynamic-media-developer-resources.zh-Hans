---
description: ZIP文件中的条目。
seo-description: ZIP文件中的条目。
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
topic: Dynamic Media Image Production System API
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

---


# ZipEntry{#zipentry}

ZIP文件中的条目。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 条目名称。 |
| `*`isDirectory`*` | `xsd:boolean` | 确定条目是否为目录。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改的日期和时间。 |
| `*`compressedSize`*` | `xsd:long` | 压缩大小。 |
| `*`uncompressedSize`*` | `xsd:long` | 未压缩大小。 |

