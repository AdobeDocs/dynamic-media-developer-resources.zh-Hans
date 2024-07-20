---
description: 资源或文件夹的磁盘空间统计信息。
solution: Experience Manager
title: 磁盘使用情况
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 10%

---

# [!DNL DiskUsage]{#diskusage}

资源或文件夹的磁盘空间统计信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司句柄。 |
| companyName | `xsd:string` | 公司名称。 |
| imageCount | `xsd:int` | 存储的图像数。 |
| 磁盘空间使用情况 | `xsd:long` | 文件端总数（以KB为单位）。 |
| lastModified | `xsd:dateTime` | 上次修改`DiskUsage`类型的日期、时间和时区。 |
