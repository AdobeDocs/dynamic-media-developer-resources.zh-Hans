---
description: 設定使用者在一或多個公司中的成員資格。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---

# setCompanyMembership{#setcompanymembership}

設定使用者在一或多個公司中的成員資格。

语法

## 授權的使用者型別 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-3930dc6a016140178631083563598104}

**輸入(setCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:sting` | 否 | 使用者控制代碼。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 許多公司。 |

**輸出(setCompanyMembershipParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-862c0cc32ce0407ab248028e690a8386}

此程式碼範例會將使用者新增至公司。 如有需要，在公司處理陣列中指定多個公司。

**请求**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**响应**

无。
