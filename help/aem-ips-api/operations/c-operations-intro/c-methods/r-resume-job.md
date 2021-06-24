---
description: 重新启动已暂停的作业。
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---

# resumeJob{#resumejob}

重新启动已暂停的作业。

语法

## 授权用户类型 {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**输入(resumeJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要重新启动的作业的公司的句柄。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 已暂停作业的句柄。 |

**输出(resumeJobReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-d0524e031f1f43d89430eade19526162}

此代码示例可重新启动暂停的作业。

**请求**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**响应**

无。
