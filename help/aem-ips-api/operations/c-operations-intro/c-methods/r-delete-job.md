---
description: 删除当前或计划的作业。
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 12%

---


# deleteJob{#deletejob}

删除当前或计划的作业。

语法

## 授权用户类型{#section-1b959679dc8147c291126ddf7e061742}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 作业所属公司的句柄。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 要删除的作业的句柄。 |

**输出**

IPS API不返回此操作的响应。

## 示例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此代码示例将删除正在运行或计划在IPS中运行的作业。 它需要一个作业句柄，您必须从其他操作获取该句柄。

**请求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**响应**

无。
