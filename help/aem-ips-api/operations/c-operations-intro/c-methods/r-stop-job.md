---
description: 停止正在进行的作业。
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---


# stopJob{#stopjob}

停止正在进行的作业。

语法

## 授权用户类型{#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2b64f074e37c4c38849994f3bc65342a}

**Input(stopJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`jobHandle`*` | `xsd:string` | 是 | 处理要停止的工作。 |

**输出(stopJobReturn0**

IPS API不返回此操作的响应。

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
