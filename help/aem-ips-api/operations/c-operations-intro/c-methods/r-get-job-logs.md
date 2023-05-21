---
description: 取得所選公司的指定工作記錄檔。 您可以依字元、方向、開始和結束日期以及列數排序。
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 11%

---

# getJobLogs{#getjoblogs}

取得所選公司的指定工作記錄檔。 您可以依字元、方向、開始和結束日期以及列數排序。

语法

## 授權的使用者型別 {#section-9df82972265d44c9ad91504a17c3ffa6}

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

**輸入(getJobLogsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 公司控點。 |
| userHandle | `xsd:string` | 否 | 取得特定使用者所提交工作的記錄。 |
| sortby | `xsd:string` | 否 | 可讓您選取排序欄位。 |
| sortDirection | `xsd:string` | 否 | 排序順序（升序或降序）。 |
| startDate | `xsd:dateTime` | 否 | 工作記錄的開始日期和時間。 提供此欄位請求的時區。 |
| endDate | `xsd:dateTime` | 否 | 工作記錄結束的日期和時間。 提供此欄位請求的時區。 |
| numRows | `xsd:int` | 否 | 要傳回的最大列數。 |

**輸出(getJobLogsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | 是 | 工作記錄陣列。 |

## 示例 {#section-35871c94b4a44559912577efddbc46a6}

此程式碼範例會傳回特定公司的IPS工作記錄檔。 您也可以使用它來傳回特定使用者或公司和使用者的工作記錄。

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
