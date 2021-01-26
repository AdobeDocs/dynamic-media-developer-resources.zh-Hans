---
description: 将用户添加到一个或多个公司。
solution: Experience Manager
title: addCompanyMembership
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---


# addCompanyMembership{#addcompanymembership}

将用户添加到一个或多个公司。

语法

## 授权用户类型{#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**输入(addCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要添加其会员资格的用户的句柄。 |
| `*`membersArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 要将用户添加到的公司的数组。 |

**输出(addCompanyMembershipReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-5469f88bac7047cca131faa6b021e437}

此示例使用`*`companyHandleArray`*`将用户添加到单个公司。

**请求**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**响应**

无。
