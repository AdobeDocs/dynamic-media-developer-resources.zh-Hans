---
description: 从一个或多个公司中删除用户。
seo-description: 从一个或多个公司中删除用户。
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Dynamic Media Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# removeCompanyMembership{#removecompanymembership}

从一个或多个公司中删除用户。

语法

## 授权用户类型{#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6dfce5e44d8a4799afd0c231a0b10463}

**输入(removeCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要删除的成员资格的用户的句柄。 |
| `*`companyHandleArray`*` | `types:HandleArray` | 是 | 要从中删除用户的公司的句柄。 |

**输出(removeCompanyMembershipReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-6b7903195e8647a1bd0502f87387ca62}

此代码示例从公司中删除用户。 忽略可选的用户句柄，从公司句柄数组中指定的公司中删除所有用户。

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
