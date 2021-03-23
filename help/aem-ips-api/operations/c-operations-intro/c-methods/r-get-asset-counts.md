---
description: 获取与特定公司关联的资产和资产数量。
seo-description: 获取与特定公司关联的资产和资产数量。
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# getAssetCounts{#getassetcounts}

获取与特定公司关联的资产和资产数量。

返回的`countArray`由`assetTypes`（数据类型`xsd:string`）的数组组成，每个数组都有自己的计数字段（数据类型`xsd:int`），允许每个数组元素表示多个资源类型。
语法

## 授权用户类型{#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**输入(getAssetCountsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要计数资产的公司的句柄。 |

**输出(getAssetCountsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | 否 | 资产类型的数组，每个资产类型都有其自己的计数字段，允许对数组中每个元素表示多个资产类型。 |

## 示例 {#section-6052a503eb3843f6adb99e200fdba280}

此代码示例将公司的句柄用作发送到IPS Web服务器的`getAssetCountsParam`中的字段，以获取资产计数。

**请求**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**响应**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

