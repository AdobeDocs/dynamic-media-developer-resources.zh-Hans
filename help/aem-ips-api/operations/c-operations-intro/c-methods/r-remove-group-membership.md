---
description: 从一组组中删除用户。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 892ee01c-e07b-4321-b0b7-5bb606036340
TQID: 'https://experienceleague.adobe.com/-RTuwtlTpQdiS-H-lf9BhQwbkp5McXo4tbxssF-0wzo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 102
ht-degree: 8%

---

# removeGroupMembership{#removegroupmembership}

从一组组中删除用户。

删除命令之间的&#x200B;**差异**

* `removeGroupMembers`：从一个组中删除多个用户。
* `removeGroupMembership`：从组数组中移除单个用户。

## 授权用户类型 {#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**输入(removeGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 您要删除其组成员资格的公司的句柄。 |
| groupHandleArray | `types:HandleArray` | 是 | 您希望从中删除公司的组的句柄数组。 |

**输出(removeGroupMembershipReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-f8d4181170a243efb9faf5824ae96197}

此代码示例从一个组中删除一个用户。

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
