---
description: 获取所有当前活动的作业。
seo-description: 获取所有当前活动的作业。
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 14%

---


# getActiveJobs{#getactivejobs}

获取所有当前活动的作业。

语法

## 授权用户类型{#section-125557a6ea7b4fc894d4bb468cd02118}

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
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的手柄。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 工作的处理。 |
| `*`originalName`*` | `xsd:string` | 否 | 原始作业名称。 |

**输出(getActiveJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | 是 | 活动作业的数组。 |

## 示例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代码示例返回在IPS中运行的公司的所有活动作业。 在这种情况下，响应是不正常的，因为IPS调度协调器在没有运行活动作业的情况下被禁用。 在正常情况下，这种反应会返回一些活跃的工作。

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

