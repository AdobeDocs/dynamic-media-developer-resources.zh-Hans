---
description: 作业运行后的作业日志。
seo-description: 作业运行后的作业日志。
seo-title: 作业日志
solution: Experience Manager
title: 作业日志
topic: Scene7 Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 作业日志{#joblog}

作业运行后的作业日志。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 公司手柄。 |
| ` *`jobHandle`*` | `xsd:string` | 工作负责人。 |
| ` *`jobName`*` | `xsd:string` | 作业名称. |
| ` *`originalJobName`*` | `xsd:string` | 为作业提交的原始名称 `submitJob`。 |
| ` *`submitUserEmail`*` | `xsd:string` | 提交作业的用户的电子邮件地址。 |
| ` *`logType`*` | `xsd:string` | 作业日志类型的选择。 |
| ` *`jobSubType`*` | `xsd:string` | 其他作业信息。 |
| ` *`startDate`*` | `xsd:dateTime` | 作业的开始日期、时间和时区。 |
| ` *`endDate`*` | `xsd:dateTime` | 作业的结束日期、时间和时区。 |
| ` *`描述`*` | `xsd:string` | 最初在中指定的作业说明 `submitJob`。 |
| ` *`fileSuccessCount`*` | `xsd:int` | 已成功处理的文件数。 |
| ` *`fileErrorCount`*` | `xsd:int` | 导致错误的文件数。 |
| ` *`fileWarningCount`*` | `xsd:int` | 生成警告的文件数。 |
| ` *`fileDuplicateCount`*` | `xsd:int` | 重复文件数。 |
| ` *`fileUpdateCount`*` | `xsd:int` | 已更新的文件数。 |
| ` *`totalFileCount`*` | `xsd:int` | 已记录作业处理的文件数。 |
| ` *`transferSuccessCount`*` | `xsd:int` | 成功转让的数量。 |
| ` *`transferErrorCount`*` | `xsd:int` | 传输错误数。 |
| ` *`transferWarningCount`*` | `xsd:int` | 传输警告数。 |
| ` *`fatalError`*` | `xsd:boolean` | 作业是否生成了致命错误。 |
| ` *`detailTotalRows`*` | `xsd:int` | 与查询匹配的总行数，由于页面大小限制，总行数可 `detailArray` 能大于大小。 |
| ` *`detailArray`*` | `types:JobLogDetailArray` | 已记录作业的详细信息数组。 |

