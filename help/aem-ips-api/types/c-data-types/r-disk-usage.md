---
description: 资源或文件夹的磁盘空间统计信息。
solution: Experience Manager
title: 磁盘使用情况
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
TQID: 'https://experienceleague.adobe.com/Md0oAgpJDqSrn1JRZsebpaZKeXIAoLcgkC5KPaHad5s'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 50
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
