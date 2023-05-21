---
description: 從群組陣列中移除使用者。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 10%

---

# removeGroupMembership{#removegroupmembership}

從群組陣列中移除使用者。

**移除命令之間的差異**

* `removeGroupMembers`：從群組移除多個使用者。
* `removeGroupMembership`：從群組陣列中移除個別使用者。

## 授權的使用者型別 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**輸入(removeGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要移除其群組成員資格之公司的控制代碼。 |
| groupHandleArray | `types:HandleArray` | 是 | 您要從中移除公司的群組的控制代碼陣列。 |

**輸出(removeGroupMembershipReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-f8d4181170a243efb9faf5824ae96197}

此程式碼範例會從群組中移除使用者。

**请求**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**响应**

无。
