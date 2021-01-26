---
description: 从特定组中删除公司用户。
seo-description: 从特定组中删除公司用户。
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Dynamic Media Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 9%

---


# removeGroupMembers{#removegroupmembers}

从特定组中删除公司用户。

**删除命令之间的差异**

* `removeGroupMembers`:从组中删除多个用户。
* `removeGroupMembership`:从一组组中删除单个用户。

## 授权用户类型{#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b5596614a3be4ce5962455884e4636af}

**输入(removeGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 与要处理的用户公司的句柄。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 组句柄。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 要删除组成员关系的用户的句柄数组。 |

**输出(removeGroupMembersParam)**

IPS API不返回此操作的响应。

## 示例 {#section-9eedac852cea46ec80de6a6928bf97ac}

此代码示例从指定公司中删除用户。 使用用户句柄数组从组中删除多个用户。

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
