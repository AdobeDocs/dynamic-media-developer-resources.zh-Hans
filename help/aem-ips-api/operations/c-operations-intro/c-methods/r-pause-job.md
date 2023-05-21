---
description: 暫停作用中的工作。
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 19%

---

# pauseJob{#pausejob}

暫停作用中的工作。

语法

## 授權的使用者型別 {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7aedb924cf8b4e05a0dc927636d537a0}

**輸入(pauseJobParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| jobHandle | `xsd:string` | 是 | 處理您要暫停的工作。 |

**輸出(PauseJobReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-ee4914f9496f4bd88556728a48fb22c1}

此程式碼範例會暫停作用中的工作。

**请求**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**响应**

无。
