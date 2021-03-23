---
description: 从一组组中删除用户。
seo-description: 从一组组中删除用户。
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 9%

---


# removeGroupMembership{#removegroupmembership}

从一组组中删除用户。

**删除命令之间的差异**

* `removeGroupMembers`:从组中删除多个用户。
* `removeGroupMembership`:从一组组中删除单个用户。

## 授权用户类型{#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**输入(removeGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要删除其用户组成员身份的公司的处理。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 要从中删除公司的组的句柄数组。 |

**输出(removeGroupMembershipReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-f8d4181170a243efb9faf5824ae96197}

此代码示例从组中删除用户。

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
