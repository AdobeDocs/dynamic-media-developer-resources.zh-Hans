---
description: 暂停活动作业。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 18%

---

# pauseJob{#pausejob}

暂停活动作业。

语法

## 授权用户类型 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7aedb924cf8b4e05a0dc927636d537a0}

**输入(pauseJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对公司负责。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 处理要暂停的作业。 |

**输出(PauseJobReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此代码示例会暂停活动作业。

**请求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**响应**

无。
