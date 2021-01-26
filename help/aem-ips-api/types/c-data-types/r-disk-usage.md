---
description: 资产或文件夹的磁盘空间统计信息。
seo-description: 资产或文件夹的磁盘空间统计信息。
seo-title: 磁盘使用
solution: Experience Manager
title: 磁盘使用
topic: Dynamic Media Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# DiskUsage{#diskusage}

资产或文件夹的磁盘空间统计信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司手柄。 |
| `*`companyName`*` | `xsd:string` | 公司名称. |
| `*`imageCount`*` | `xsd:int` | 存储的图像数。 |
| `*`diskSpaceUsage`*` | `xsd:long` | 文件端总数(KB)。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改`DiskUsage`类型的日期、时间和时区。 |

