---
description: 设置属于特定公司的用户的用户组成员关系。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

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
