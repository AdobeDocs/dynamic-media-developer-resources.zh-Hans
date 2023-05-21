---
description: 設定屬於特定公司之使用者的群組成員資格。
solution: Experience Manager
title: setgroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 9%

---

# setgroupMembers{#setgroupmembers}

設定屬於特定公司之使用者的群組成員資格。

如果您沒有完成此作業的許可權，作業會擲回驗證錯誤。 如果使用者控制代碼陣列中的任何使用者不屬於公司控制代碼中指定的公司，也是如此。

## 授權的使用者型別 {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6a18562fc8e942af94be10bbb8c51151}

**輸入(setGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| groupHandle | `xsd:string` | 是 | 群組控制代碼。 |
| userHandleArray | `types:HandleArray` | 是 | 您要設定其群組成員資格的使用者之控制代碼陣列。 |

**輸出(setGroupMembesReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此程式碼範例為單一使用者設定群組成員資格。

**请求**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**响应**

无。
