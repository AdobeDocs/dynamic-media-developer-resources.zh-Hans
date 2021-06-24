---
description: 获取计划运行的作业。
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 21%

---

# getScheduledJobs{#getscheduledjobs}

获取计划运行的作业。

语法

## 授权用户类型 {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2af604ff8282460990b9237158187f8f}

**输入(getScheduledJobsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 作业处理。 |
| `*`originalName`*` | `xsd:string` | 否 | `submitJob`指定的名称。 |

**Output(getScheduledJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | 是 | 计划作业的数组。 |

## 示例 {#section-e79e7da86ba848fd9996aa36de462e6c}

此代码示例返回作业数组中的所有计划作业。 阵列本身包含有关作业的详细信息。

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
