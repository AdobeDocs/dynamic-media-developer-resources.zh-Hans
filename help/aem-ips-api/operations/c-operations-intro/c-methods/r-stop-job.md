---
description: 停止正在进行的作业。
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 22%

---

# stopJob{#stopjob}

停止正在进行的作业。

语法

## 授权用户类型 {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2b64f074e37c4c38849994f3bc65342a}

**输入(stopJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司处理。 |
| jobHandle | `xsd:string` | 是 | 处理要停止的作业。 |

**输出(stopJobReturn0**

IPS API未返回此操作的响应。

## 示例 {#section-f7e07fa09ae24dc89685533f20ab3b81}

**请求**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**响应**

无。
