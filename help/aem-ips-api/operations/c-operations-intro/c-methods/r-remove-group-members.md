---
description: 從特定群組移除公司使用者。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 10%

---

# removeGroupMembers{#removegroupmembers}

從特定群組移除公司使用者。

**移除命令之間的差異**

* `removeGroupMembers`：從群組移除多個使用者。
* `removeGroupMembership`：從群組陣列中移除個別使用者。

## 授權的使用者型別 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b5596614a3be4ce5962455884e4636af}

**輸入(removeGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 含有您要使用之使用者的公司控制代碼。 |
| groupHandle | `xsd:string` | 是 | 群組控制代碼。 |
| userHandleArray | `types:HandleArray` | 是 | 您要移除其群組成員資格之使用者的控制代碼陣列。 |

**輸出(removeGroupMembersParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此程式碼範例會從指定的公司移除使用者。 從具有使用者控制代碼陣列的群組中移除多個使用者。

**请求**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**响应**

无。
