---
description: 设置用户的组成员资格。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# setGroupMembership{#setgroupmembership}

设置用户的组成员资格。

语法

## 授权用户类型 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**输入(setGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要设置其群组成员资格的用户的句柄。 |
| `*`companyHandle`*` | `xsd:string` | 否 | 公司负责人。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 用户所属的组的句柄数组。 |

**Output(setGroupMembershipReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-67b86d259df24938896fe19061845811}

此代码示例使用户成为组的成员。 使用组句柄数组将用户添加到多个组。

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
