---
description: 返回按资源类型分组的所有元数据字段。
solution: Experience Manager
title: getAssetMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---

# getAssetMetadataField{#getassetmetadatafields}

返回按资源类型分组的所有元数据字段。

语法

## 授权用户类型 {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**输入(getAssetMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 要检索其元数据的公司的句柄。 |

**输出(getAssetMetadataFieldsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | 是 | 按资源类型排列的元数据字段数组。 |

## 示例 {#section-d79ab85f29144635b0b61416e52f4f3f}

**请求**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**响应**

>[!NOTE]
>
>为简短起见，已截断。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
