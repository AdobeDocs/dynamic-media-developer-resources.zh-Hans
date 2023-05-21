---
description: 從一或多個公司移除使用者。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 12%

---

# removeCompanyMembership{#removecompanymembership}

從一或多個公司移除使用者。

语法

## 授權的使用者型別 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**輸入(removeCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 具有您要移除之成員資格的使用者的控制代碼。 |
| companyHandleArray | `types:HandleArray` | 是 | 您要從中移除使用者的公司的控制代碼。 |

**輸出(removeCompanyMembershipReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-6b7903195e8647a1bd0502f87387ca62}

此程式碼範例會從公司中移除使用者。 省略選用的使用者控制代碼，從公司控制代碼陣列中指定的公司中移除所有使用者。

**请求**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**响应**

无。
