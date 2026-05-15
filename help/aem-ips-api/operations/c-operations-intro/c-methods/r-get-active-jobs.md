---
description: 获取当前所有活动的作业。
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 14%

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
| companyHandle | `xsd:string` | 否 | 公司的把手。 |
| jobHandle | `xsd:string` | 否 | 作业的句柄。 |
| 原始名称 | `xsd:string` | 否 | 原始作业名称。 |

**输出(getActiveJobsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| jobArray | `xsd:string` | 是 | 活动作业的数组。 |

## 示例 {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

此代码示例返回公司在IPS中运行的所有活动作业。 在这种情况下，响应不正常，因为IPS计划协调器已禁用，且没有活动作业正在运行。 在正常情况下，响应将返回大量活动作业。

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
