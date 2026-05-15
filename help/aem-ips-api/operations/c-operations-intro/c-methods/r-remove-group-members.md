---
description: 从特定组中删除公司用户。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
TQID: 'https://experienceleague.adobe.com/dMEOhQgXQvFvZj2Kozsq6J7qJNiwYpknQQbNkADMsg0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 8%

---

# removeGroupMembers{#removegroupmembers}

从特定组中删除公司用户。

删除命令之间的&#x200B;**差异**

* `removeGroupMembers`：从一个组中删除多个用户。
* `removeGroupMembership`：从组数组中移除单个用户。

## 授权用户类型 {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b5596614a3be4ce5962455884e4636af}

**输入(removeGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要处理的用户的公司的句柄。 |
| groupHandle | `xsd:string` | 是 | 组句柄。 |
| userHandleArray | `types:HandleArray` | 是 | 您要删除其组成员资格的用户句柄数组。 |

**输出(removeGroupMembersParam)**

IPS API不返回此操作的响应。

## 示例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此代码示例从指定的公司中删除用户。 从具有用户句柄数组的组中删除多个用户。

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
