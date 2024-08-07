---
description: 设置属于特定公司的用户的组成员资格。
solution: Experience Manager
title: setgroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 7%

---

# setgroupMembers{#setgroupmembers}

设置属于特定公司的用户的组成员资格。

如果您没有完成此操作的权限，则此操作会引发身份验证错误。 如果用户句柄数组中的任何用户不属于公司句柄中指定的公司，也是如此，

## 授权用户类型 {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6a18562fc8e942af94be10bbb8c51151}

**输入(setGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司句柄。 |
| groupHandle | `xsd:string` | 是 | 组句柄。 |
| userHandleArray | `types:HandleArray` | 是 | 要为其设置组成员资格的用户句柄数组。 |

**输出(setGroupMembesReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-9c528c3f44a141ce9eaddf634f26c487}

此代码示例为单个用户设置组成员资格。

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
