---
description: 设置属于特定公司的用户的用户组成员关系。
seo-description: 设置属于特定公司的用户的用户组成员关系。
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 8%

---


# setGroupMembers{#setgroupmembers}

设置属于特定公司的用户的用户组成员关系。

如果您没有完成此操作的权限，该操作将引发身份验证错误。 如果用户句柄数组中的任何用户不属于公司句柄中指定的公司，则也是如此。

## 授权用户类型{#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6a18562fc8e942af94be10bbb8c51151}

**Input(setGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 组句柄。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 要设置其用户组成员关系的用户的句柄数组。 |

**输出(setGroupMembersReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此代码示例设置单个用户的用户组成员关系。

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
