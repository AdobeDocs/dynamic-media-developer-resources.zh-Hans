---
description: 作业运行后的作业日志。
solution: Experience Manager
title: 作业日志
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---

# [!DNL JobLog]{#joblog}

作业运行后的作业日志。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| companyHandle | `xsd:string` | 公司句柄。 |
| jobHandle | `xsd:string` | 作业句柄。 |
| jobName | `xsd:string` | 作业名称。 |
| 原始作业名称 | `xsd:string` | 使用`submitJob`提交的作业的原始名称。 |
| submitUserEmail | `xsd:string` | 提交作业的用户的电子邮件地址。 |
| logType | `xsd:string` | 作业日志类型的选择。 |
| 作业子类型 | `xsd:string` | 其他作业信息。 |
| startDate | `xsd:dateTime` | 作业的开始日期、时间和时区。 |
| endDate | `xsd:dateTime` | 作业的结束日期、时间和时区。 |
| [!DNL description] | `xsd:string` | 最初在`submitJob`中指定的作业的描述。 |
| fileSuccessCount | `xsd:int` | 成功处理的文件数。 |
| fileErrorcount | `xsd:int` | 导致错误的文件数。 |
| fileWarningCount | `xsd:int` | 生成警告的文件数。 |
| fileDuplicateCount | `xsd:int` | 重复文件数。 |
| fileUpdateCount | `xsd:int` | 已更新的文件数。 |
| totalfilecount | `xsd:int` | 记录的作业处理的文件数。 |
| Transfersuccesscount | `xsd:int` | 成功传输的次数。 |
| Transferrorcount | `xsd:int` | 传输错误数。 |
| transferWarningCount | `xsd:int` | 传输警告数。 |
| fatalError | `xsd:boolean` | 作业是否生成了致命错误。 |
| detailTotalRows | `xsd:int` | 与查询匹配的总行数，由于页面大小限制，可能大于`detailArray`的大小。 |
| detailarray | `types:JobLogDetailArray` | 有关已记录作业的详细信息数组。 |
