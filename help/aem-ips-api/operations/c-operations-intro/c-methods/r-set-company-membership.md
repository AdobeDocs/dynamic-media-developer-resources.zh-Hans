---
description: 在一个或多个公司中设置用户的成员资格。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembership{#setcompanymembership}

在一个或多个公司中设置用户的成员资格。

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
| `*`userHandle`*` | `xsd:sting` | 否 | 用户句柄。 |
| `*`membersingArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 一系列公司。 |

**输出(setCompanyMembershipParam)**

IPS API不会返回此操作的响应。

## 示例 {#section-862c0cc32ce0407ab248028e690a8386}

此代码示例可将用户添加到公司。 根据需要，指定公司句柄数组中的多个公司。

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
