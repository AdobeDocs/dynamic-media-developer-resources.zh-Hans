---
description: 将特定公司的用户添加到特定组。
solution: Experience Manager
title: addGroupMembers
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---


# addGroupMembers{#addgroupmembers}

将特定公司的用户添加到特定组。

语法

## 授权用户类型{#section-b4406c54ed7c4827be4c1acc957e0057}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-b28434dcf2ca4b4ea431136aac33913e}

**输入(addGroupMembersParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`groupHandle`*` | `xsd:string` | 是 | 组句柄。 |
| `*`userHandleArray`*` | `types:HandleArray` | 是 | 要添加到组的用户的句柄数组。 |

**输出(addGroupMembersParam)**

IPS API不返回此操作的响应。

## 示例 {#section-8f168b528aef4c4fa8c3d41f7686842f}

此示例使用`*`addGroupMembersParam`*`将用户添加到单个公司。 IPS API不返回此操作的响应。

**请求**

```java
<ns1:addGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
<ns1:userHandleArray><ns1:items>70|kmagnusson@adobe.com</ns1:items></ns1:userHandleArray>
</ns1:addGroupMembersParam>
```

**响应**

无。
