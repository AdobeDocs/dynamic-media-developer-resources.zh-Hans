---
description: 取得排定要執行的工作。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 22%

---

# getScheduledJobs{#getscheduledjobs}

取得排定要執行的工作。

语法

## 授權的使用者型別 {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2af604ff8282460990b9237158187f8f}

**輸入(getScheduledJobsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| jobHandle | `xsd:string` | 否 | 工作控制代碼。 |
| 原始名稱 | `xsd:string` | 否 | 指定的名稱 `submitJob`. |

**輸出(getScheduledJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | 是 | 排程工作的陣列。 |

## 示例 {#section-e79e7da86ba848fd9996aa36de462e6c}

此程式碼範例會傳回工作陣列中的所有排程工作。 陣列本身包含有關作業的詳細資訊。

**请求**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**响应**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```
