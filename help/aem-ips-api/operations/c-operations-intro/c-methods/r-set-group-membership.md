---
description: 设置用户的用户组成员关系。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---


# setGroupMembership{#setgroupmembership}

设置用户的用户组成员关系。

语法

## 授权用户类型{#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-6aeda13b26af4796aad1306ac7a9ad17}

**输入(setGroupMembershipParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 要设置其用户组成员关系的用户的句柄。 |
| `*`companyHandle`*` | `xsd:string` | 否 | 公司手柄。 |
| `*`groupHandleArray`*` | `types:HandleArray` | 是 | 用户所属的组的句柄数组。 |

**输出(setGroupMembershipReturn)**

IPS API不返回此操作的响应。

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
