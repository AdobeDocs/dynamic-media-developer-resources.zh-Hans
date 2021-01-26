---
description: 获取选定公司的指定作业日志。 您可以按字符、方向、开始和结束日期以及行数排序。
seo-description: 获取选定公司的指定作业日志。 您可以按字符、方向、开始和结束日期以及行数排序。
seo-title: getJobLogs
solution: Experience Manager
title: getJobLogs
topic: Dynamic Media Image Production System API
uuid: 850ccfad-6cdb-4eda-a20a-762fadadf8b2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 10%

---


# getJobLogs{#getjoblogs}

获取选定公司的指定作业日志。 您可以按字符、方向、开始和结束日期以及行数排序。

语法

## 授权用户类型{#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8cfdc7994da24678a45edcb37e9a2166}

**输入(getJobLogsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 公司手柄。 |
| `*`userHandle`*` | `xsd:string` | 否 | 获取特定用户提交的作业的日志。 |
| `*`排序依据`*` | `xsd:string` | 否 | 允许您选择排序字段。 |
| `*`sortDirection`*` | `xsd:string` | 否 | 排序顺序（升序或降序）。 |
| `*`startDate`*` | `xsd:dateTime` | 否 | 作业日志开始的日期和时间。 为时区提供此字段的请求。 |
| `*`endDate`*` | `xsd:dateTime` | 否 | 作业日志结束的日期和时间。 为时区提供此字段的请求。 |
| `*`numRows`*` | `xsd:int` | 否 | 要返回的最大行数。 |

**输出(getJobLogsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobLogArray`*` | `types: JobLogArray` | 是 | 作业日志的数组。 |

## 示例 {#section-35871c94b4a44559912577efddbc46a6}

此代码示例返回特定公司的IPS作业日志。 您还可以使用它返回特定用户或公司和用户的作业日志。

**请求**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**响应**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```

