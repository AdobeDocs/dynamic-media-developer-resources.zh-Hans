---
description: 暂停活动作业。
seo-description: 暂停活动作业。
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 16%

---


# pauseJob{#pausejob}

暂停活动作业。

语法

## 授权用户类型{#section-f2bf306ab4574871bd21f9f7dd681033}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 处理公司。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 处理要暂停的作业。 |

**输出(PauseJobReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此代码示例暂停活动作业。

**请求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**响应**

无。
