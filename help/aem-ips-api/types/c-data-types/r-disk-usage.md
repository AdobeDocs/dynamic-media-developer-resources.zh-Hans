---
description: 资产或文件夹的磁盘空间统计信息。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

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

