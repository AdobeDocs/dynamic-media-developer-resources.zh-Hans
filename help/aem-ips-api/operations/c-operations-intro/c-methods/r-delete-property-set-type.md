---
description: 删除属性集类型及其关联的属性集和属性。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

删除属性集类型及其关联的属性集和属性。

语法

## 授权用户类型 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-1c8973f5d35f44b4a6a483a41609e455}

**Input(deletePropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | 是 | 要删除的属性集类型的句柄。 |

**输出(deletePropertySetTypeParam)**

IPS API不会返回此操作的响应。

## 示例 {#section-85faa2e3411a4e23aa6489037f7ce078}

此代码示例将类型的句柄用作发送到IPS Web服务服务器的`deletePropertySetTypeParam`中的字段，以删除属性集类型。

**请求**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**响应**

无。
