---
description: 新增使用者至一或多間公司。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---

# addCompanyMembership{#addcompanymembership}

新增使用者至一或多間公司。

语法

## 授權的使用者型別 {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**輸入(addCompanyMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要新增其成員資格之使用者的控制代碼。 |
| memberlationarray | `types:CompanyMembershipUpdateArray` | 是 | 您要新增使用者的許多公司。 |

**輸出(addCompanyMembershipReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-5469f88bac7047cca131faa6b021e437}

此範例使用companyHandleArray將使用者新增至單一公司。

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
