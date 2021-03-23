---
description: ZIP文件中的条目。
seo-description: ZIP文件中的条目。
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

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
| `*`uncompressedSize`*` | `xsd:long` | 未压缩的大小。 |

