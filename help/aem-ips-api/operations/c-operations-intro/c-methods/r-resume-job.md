---
description: 重新启动暂停的作业。
seo-description: 重新启动暂停的作业。
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
topic: Dynamic Media Image Production System API
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 16%

---


# resumeJob{#resumejob}

重新启动暂停的作业。

语法

## 授权用户类型{#section-eab49f4b6d1041179000326a10fee889}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 要重新启动的作业的公司的句柄。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 暂停作业的句柄。 |

**输出(resumeJobReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-d0524e031f1f43d89430eade19526162}

此代码示例重新启动暂停的作业。

**请求**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**响应**

无。
