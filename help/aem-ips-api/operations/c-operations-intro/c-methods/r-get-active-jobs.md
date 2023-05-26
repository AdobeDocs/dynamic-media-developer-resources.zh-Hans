---
description: 获取所有当前活动的作业。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

获取所有当前活动的作业。

语法

## 授权用户类型 {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**输入(getActiveJobsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 公司的把手。 |
| jobHandle | `xsd:string` | 否 | 作业的句柄。 |
| 原始名称 | `xsd:string` | 否 | 原始作业名称。 |

**输出(getActiveJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobArray | `xsd:string` | 是 | 活动作业的数组。 |

## 示例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代码示例返回公司在IPS中运行的所有活动作业。 在这种情况下，响应不寻常，因为IPS调度协调器被禁用，且没有活动作业正在运行。 在正常情况下，响应将返回大量活动作业。

**请求**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**响应**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```
