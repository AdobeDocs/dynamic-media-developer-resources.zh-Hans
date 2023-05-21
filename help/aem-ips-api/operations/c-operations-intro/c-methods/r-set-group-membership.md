---
description: 設定使用者的群組成員資格。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 13%

---

# setGroupMembership{#setgroupmembership}

設定使用者的群組成員資格。

语法

## 授權的使用者型別 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**輸入(setGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要設定其群組成員資格之使用者的控制代碼。 |
| companyHandle | `xsd:string` | 否 | 公司控點。 |
| groupHandleArray | `types:HandleArray` | 是 | 使用者所屬群組的控制代碼陣列。 |

**輸出(setGroupMembershipReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-67b86d259df24938896fe19061845811}

此程式碼範例將使用者設為群組的成員。 使用群組控制代碼陣列將使用者新增至多個群組。

**请求**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**响应**

无。
