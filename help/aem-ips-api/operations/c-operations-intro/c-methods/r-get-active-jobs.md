---
description: 获取当前所有活动的作业。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 16%

---

# getActiveJobs{#getactivejobs}

获取当前所有活动的作业。

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
| `*`companyHandle`*` | `xsd:string` | 否 | 公司的把手。 |
| `*`jobHandle`*` | `xsd:string` | 否 | 工作的把手。 |
| `*`originalName`*` | `xsd:string` | 否 | 原始作业名称。 |

**Output(getActiveJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | 是 | 活动作业数组。 |

## 示例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代码示例返回在IPS中运行的公司的所有活动作业。 在这种情况下，响应异常，因为IPS调度协调器处于禁用状态，且未运行活动作业。 在正常情况下，响应将返回多个活动作业。

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
