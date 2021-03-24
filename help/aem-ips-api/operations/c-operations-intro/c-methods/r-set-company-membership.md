---
description: 在一个或多个公司中设置用户的会员资格。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---


# setCompanyMembership{#setcompanymembership}

在一个或多个公司中设置用户的会员资格。

语法

## 授权用户类型{#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-3930dc6a016140178631083563598104}

**输入(setCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | 否 | 用户句柄。 |
| `*`membershArray`*` | `types:CompanyMembershipUpdateArray` | 是 | 公司数组。 |

**输出(setCompanyMembershipParam)**

IPS API不返回此操作的响应。

## 示例 {#section-862c0cc32ce0407ab248028e690a8386}

此代码示例将用户添加到公司。 如果需要，在公司句柄数组中指定多个公司。

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
