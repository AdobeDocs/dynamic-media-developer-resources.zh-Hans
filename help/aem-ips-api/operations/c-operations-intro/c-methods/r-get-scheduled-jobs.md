---
description: 获取计划运行的作业。
seo-description: 获取计划运行的作业。
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 19%

---


# getScheduledJobs{#getscheduledjobs}

获取计划运行的作业。

语法

## 授权用户类型{#section-bd1835ab508a429f8143b3bdb811d6a4}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的手柄。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 工作。 |
| `*`originalName`*` | `xsd:string` | 否 | 由`submitJob`指定的名称。 |

**输出(getScheduledJobsReturn)**

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

