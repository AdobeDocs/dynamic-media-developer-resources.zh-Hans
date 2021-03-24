---
description: 删除属性集和所有关联属性。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

---


# deletePropertySet{#deletepropertyset}

删除属性集和所有关联属性。

语法

## 授权用户类型{#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e5fc868f69494cf6858e03027db09101}

**Input(deletePropertySetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | 是 | 要删除的属性集的句柄。 |

**输出(deletePropertySetParam)**

IPS API不返回此操作的响应。

## 示例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

此代码示例将集的句柄用作发送到IPS Web服务器的`deletePropertySetParam`中的字段，以删除属性集。

**请求**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**响应**

无。
