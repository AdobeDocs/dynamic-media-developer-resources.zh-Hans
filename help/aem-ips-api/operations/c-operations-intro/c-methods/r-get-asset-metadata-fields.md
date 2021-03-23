---
description: 返回按资产类型分组的所有元数据字段。
seo-description: 返回按资产类型分组的所有元数据字段。
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
feature: Dynamic Media Classic，SDK/API，元数据，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 18%

---


# getAssetMetadataFields{#getassetmetadatafields}

返回按资产类型分组的所有元数据字段。

语法

## 授权用户类型{#section-e19a9d21cc2b45469c233d4ae55ebfc2}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 要检索其元数据的公司的句柄。 |

**输出(getAssetMetadataFieldsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | 是 | 元数据字段的数组，按资产类型。 |

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
>短时间截断。

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

