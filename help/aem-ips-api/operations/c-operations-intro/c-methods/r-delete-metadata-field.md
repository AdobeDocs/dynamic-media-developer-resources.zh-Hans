---
description: 删除公司的元数据字段。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 10%

---


# deleteMetadataField{#deletemetadatafield}

删除公司的元数据字段。

语法

## 授权用户类型{#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-73f12a30cc4340b6b32dd11effd5195e}

**输入(deleteMetadataFieldParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要删除的元数据字段的公司的句柄。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 要删除的元数据字段的句柄。 |

**输出(deleteMetadataFieldParam)**

IPS API不返回此操作的响应。

## 示例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此代码示例将删除公司的元数据字段。 它使用公司句柄和元数据句柄作为传递到IPS Web服务器的`deleteMetadataFieldParam`中的字段来执行此操作。

**请求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**响应**

无。0
