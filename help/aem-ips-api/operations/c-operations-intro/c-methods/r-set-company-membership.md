---
description: 设置用户在一个或多个公司中的成员资格。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 13%

---

# setCompanyMembership{#setcompanymembership}

设置用户在一个或多个公司中的成员资格。

语法

## 授权用户类型 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-3930dc6a016140178631083563598104}

**输入(setCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:sting` | 否 | 用户句柄。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | 是 | 众多公司。 |

**输出(setCompanyMembershipParam)**

IPS API不返回此操作的响应。

## 示例 {#section-862c0cc32ce0407ab248028e690a8386}

此代码示例将一个用户添加到公司。 如果需要，在公司句柄阵列中指定多个公司。

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
