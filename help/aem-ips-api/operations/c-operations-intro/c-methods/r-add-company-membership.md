---
description: 将用户添加到一个或多个公司。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 12%

---

# addCompanyMembership{#addcompanymembership}

将用户添加到一个或多个公司。

语法

## 授权用户类型 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**输入(addCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 要添加其成员资格的用户的句柄。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | 是 | 要向其添加用户的一系列公司。 |

**输出(addCompanyMembershipReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-5469f88bac7047cca131faa6b021e437}

此示例使用companyHandleArray将用户添加到单个公司。

**请求**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**响应**

无。
