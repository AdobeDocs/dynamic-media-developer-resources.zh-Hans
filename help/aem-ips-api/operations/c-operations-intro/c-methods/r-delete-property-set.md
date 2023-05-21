---
description: 刪除屬性集和所有相關屬性。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 13%

---

# deletePropertySet{#deletepropertyset}

刪除屬性集和所有相關屬性。

语法

## 授權的使用者型別 {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e5fc868f69494cf6858e03027db09101}

**輸入(deletePropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| setHandle | `xsd:string` | 是 | 要刪除之屬性集的控制代碼。 |

**輸出(deletePropertySetParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此程式碼範例使用集的控點作為中的欄位 `deletePropertySetParam` 傳送至IPS Web服務伺服器，以便刪除屬性集。

**请求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**响应**

无。
