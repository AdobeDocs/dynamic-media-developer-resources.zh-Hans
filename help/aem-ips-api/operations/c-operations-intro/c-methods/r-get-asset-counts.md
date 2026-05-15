---
description: 获取与特定公司关联的资源和资源数。
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

获取与特定公司关联的资源和资源数。

返回的`countArray`由`assetTypes` （数据类型`xsd:string`）的数组组成，每个数组都有自己的计数字段（数据类型`xsd:int`），允许该数组的每个元素表示多个资产类型。
语法

## 授权用户类型 {#section-6234754722184e828352f10eb18fbce9}

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
| companyHandle | `xsd:string` | 是 | 包含要计数的资产的公司的句柄。 |

**输出(getAssetCountsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| countArray | `types:AssetCountArray` | 否 | 一个资源类型数组，每个资源类型都有自己的计数字段，允许表示数组中每个元素的多个资源类型。 |

## 示例 {#section-6052a503eb3843f6adb99e200fdba280}

此代码示例使用公司的句柄作为发送到IPS Web服务服务器的`getAssetCountsParam`中的字段以获取资产计数。

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
