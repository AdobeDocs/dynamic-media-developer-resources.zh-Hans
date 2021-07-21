---
description: ZIP文件中的条目。
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '48'
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
