---
description: 更新资产集。
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 19%

---


# updateAssetSet{#updateassetset}

更新资产集。

语法

## 参数 {#section-d7080ccd97334c94860eb107a3e132b2}

**输入(updateAssetSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要修改的图像集的公司的手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要修改的图像集的手柄。 |
| `*`setDefinition`*` | `xsd:string` | 否 | 重置图像集成员。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 用作图像集缩略图的资产手柄。 |

**输出(updateAssetSetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
|  |  |  |  |

## 示例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**请求**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**响应**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

