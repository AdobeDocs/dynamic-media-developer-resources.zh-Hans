---
description: 删除公司的元数据字段。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deleteMetadataField{#deletemetadatafield}

删除公司的元数据字段。

语法

## 授权用户类型 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-73f12a30cc4340b6b32dd11effd5195e}

**输入(deleteMetadataFieldParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要删除的元数据字段的公司的句柄。 |
| fieldHandle | `xsd:string` | 是 | 要删除的元数据字段的句柄。 |

**输出(deleteMetadataFieldParam)**

IPS API未返回此操作的响应。

## 示例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此代码示例删除公司的元数据字段。 它使用公司句柄和元数据句柄作为 `deleteMetadataFieldParam` 传递到IPS Web服务服务器以执行此操作。

**请求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**响应**

无。0
