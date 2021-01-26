---
description: 删除属性集和所有关联属性。
seo-description: 删除属性集和所有关联属性。
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Dynamic Media Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 11%

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

**输入(deletePropertySetParam)**

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
