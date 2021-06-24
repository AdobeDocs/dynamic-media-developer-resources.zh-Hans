---
description: 从一个或多个公司中删除用户。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 11%

---

# removeCompanyMembership{#removecompanymembership}

从一个或多个公司中删除用户。

语法

## 授权用户类型 {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**输入(removeCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 具有要删除的成员资格的用户的句柄。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 是 | 从中删除用户的公司的句柄。 |

**输出(removeCompanyMembershipReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-6b7903195e8647a1bd0502f87387ca62}

此代码示例可从公司中删除用户。 省略可选的用户句柄，以从公司句柄数组中指定的公司中删除所有用户。

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
