---
description: 从一组组中删除用户。
solution: Experience Manager
title: removeGroupMembership
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 10%

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
