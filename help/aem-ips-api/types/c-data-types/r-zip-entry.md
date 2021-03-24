---
description: ZIP文件中的条目。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
| `*`uncompressedSize`*` | `xsd:long` | 未压缩的大小。 |

