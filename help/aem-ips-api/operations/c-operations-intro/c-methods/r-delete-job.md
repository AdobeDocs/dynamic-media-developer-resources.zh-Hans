---
description: 删除当前作业或计划作业。
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---

# deleteJob{#deletejob}

删除当前作业或计划作业。

语法

## 授权用户类型 {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-000c42bc93744b1a8e777f3ec3c272b0}

**输入(deleteJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 作业所属公司的句柄。 |
| jobHandle | `xsd:string` | 是 | 要删除的作业的句柄。 |

**输出**

IPS API未返回此操作的响应。

## 示例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此代码示例删除正在运行或计划在IPS中运行的作业。 它需要一个作业句柄，您必须从另一个操作中获取该句柄。

**请求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**响应**

无。
