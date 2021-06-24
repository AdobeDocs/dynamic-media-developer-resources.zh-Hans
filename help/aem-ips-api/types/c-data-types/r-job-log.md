---
description: 作业运行后的作业日志。
solution: Experience Manager
title: 作业日志
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 3%

---

# 作业日志{#joblog}

作业运行后的作业日志。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司负责人。 |
| `*`jobHandle`*` | `xsd:string` | 作业处理。 |
| `*`jobName`*` | `xsd:string` | 作业名称. |
| `*`originalJobName`*` | `xsd:string` | 为`submitJob`的作业提交的原始名称。 |
| `*`submitUserEmail`*` | `xsd:string` | 提交作业的用户的电子邮件地址。 |
| `*`logType`*` | `xsd:string` | 作业日志类型的选择。 |
| `*`jobSubType`*` | `xsd:string` | 其他作业信息。 |
| `*`startDate`*` | `xsd:dateTime` | 作业的开始日期、时间和时区。 |
| `*`endDate`*` | `xsd:dateTime` | 作业的结束日期、时间和时区。 |
| `*`描述`*` | `xsd:string` | 最初在`submitJob`中指定的作业描述。 |
| `*`fileSuccessCount`*` | `xsd:int` | 已成功处理的文件数。 |
| `*`fileErrorCount`*` | `xsd:int` | 导致错误的文件数。 |
| `*`fileWarningCount`*` | `xsd:int` | 生成警告的文件数。 |
| `*`fileDuplicateCount`*` | `xsd:int` | 重复文件的数量。 |
| `*`fileUpdateCount`*` | `xsd:int` | 更新的文件数。 |
| `*`totalFileCount`*` | `xsd:int` | 已记录作业处理的文件数。 |
| `*`transferSuccessCount`*` | `xsd:int` | 成功传输的数量。 |
| `*`transferErrorCount`*` | `xsd:int` | 传输错误数。 |
| `*`transferWarningCount`*` | `xsd:int` | 传输警告的数量。 |
| `*`fatalError`*` | `xsd:boolean` | 作业是否生成致命错误。 |
| `*`detailTotalRows`*` | `xsd:int` | 与查询匹配的总行数，由于页面大小限制，该行大于`detailArray`的大小。 |
| `*`detailArray`*` | `types:JobLogDetailArray` | 有关已记录作业的详细信息数组。 |
