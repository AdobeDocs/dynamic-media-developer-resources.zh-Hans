---
description: 刪除目前或排程的工作。
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

刪除目前或排程的工作。

语法

## 授權的使用者型別 {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-000c42bc93744b1a8e777f3ec3c272b0}

**輸入(deleteJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 工作所屬公司的控制代碼。 |
| jobHandle | `xsd:string` | 是 | 要刪除之工作的控制代碼。 |

**輸出**

IPS API未傳回此作業的回應。

## 示例 {#section-732d21d4dad04337b7a5ae1a0cc00eba}

此程式碼範例會刪除正在執行或排程在IPS中執行的工作。 它需要作業控制代碼，您必須從其他作業取得此控制代碼。

**请求**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**响应**

无。
