---
description: 从组数组中删除用户。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 10%

---

# removeGroupMembership{#removegroupmembership}

从组数组中删除用户。

**删除命令之间的差异**

* `removeGroupMembers`:从群组中删除多个用户。
* `removeGroupMembership`:从组数组中删除单个用户。

## 授权用户类型 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**输入(removeGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要删除其组成员资格的公司的句柄。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 希望从中删除公司的组的句柄数组。 |

**输出(removeGroupMembershipReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-f8d4181170a243efb9faf5824ae96197}

此代码示例会从组中删除用户。

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
