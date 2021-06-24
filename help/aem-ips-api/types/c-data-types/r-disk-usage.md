---
description: 资产或文件夹的磁盘空间统计信息。
solution: Experience Manager
title: DiskUsage
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 12%

---

# DiskUsage{#diskusage}

资产或文件夹的磁盘空间统计信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司负责人。 |
| `*`companyName`*` | `xsd:string` | 公司名称. |
| `*`imageCount`*` | `xsd:int` | 存储的图像数量。 |
| `*`diskSpaceUsage`*` | `xsd:long` | 文件端总数（千字节）。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改`DiskUsage`类型的日期、时间和时区。 |
