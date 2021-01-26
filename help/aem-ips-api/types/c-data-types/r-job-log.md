---
description: 作业运行后的作业日志。
seo-description: 作业运行后的作业日志。
seo-title: 作业日志
solution: Experience Manager
title: 作业日志
topic: Dynamic Media Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 3%

---


# JobLog{#joblog}

作业运行后的作业日志。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 公司手柄。 |
| `*`jobHandle`*` | `xsd:string` | 工作。 |
| `*`jobName`*` | `xsd:string` | 作业名称. |
| `*`originalJobName`*` | `xsd:string` | 为具有`submitJob`的作业提交的原始名称。 |
| `*`submitUserEmail`*` | `xsd:string` | 提交作业的用户的电子邮件地址。 |
| `*`logType`*` | `xsd:string` | 作业日志类型的选择。 |
| `*`jobSubType`*` | `xsd:string` | 其他工作信息。 |
| `*`startDate`*` | `xsd:dateTime` | 作业的开始日期、时间和时区。 |
| `*`endDate`*` | `xsd:dateTime` | 作业的结束日期、时间和时区。 |
| `*`描述`*` | `xsd:string` | 最初在`submitJob`中指定的作业描述。 |
| `*`fileSuccessCount`*` | `xsd:int` | 成功处理的文件数。 |
| `*`fileErrorCount`*` | `xsd:int` | 导致错误的文件数。 |
| `*`fileWarningCount`*` | `xsd:int` | 生成警告的文件数。 |
| `*`fileDuplicateCount`*` | `xsd:int` | 重复文件数。 |
| `*`fileUpdateCount`*` | `xsd:int` | 已更新的文件数。 |
| `*`totalFileCount`*` | `xsd:int` | 已记录作业处理的文件数。 |
| `*`transferSuccessCount`*` | `xsd:int` | 成功传输的数量。 |
| `*`transferErrorCount`*` | `xsd:int` | 传输错误数。 |
| `*`transferWarningCount`*` | `xsd:int` | 传输警告数。 |
| `*`fatalError`*` | `xsd:boolean` | 作业是否生成致命错误。 |
| `*`detailTotalRows`*` | `xsd:int` | 与查询匹配的行总数，由于页面大小限制，其大小可能大于`detailArray`。 |
| `*`detailArray`*` | `types:JobLogDetailArray` | 已记录作业的详细信息数组。 |

