---
description: 更新資產集。
solution: Experience Manager
title: 更新資產集
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 22%

---

# 更新資產集{#updateassetset}

更新資產集。

语法

## 参数 {#section-d7080ccd97334c94860eb107a3e132b2}

**輸入(updateAssetSetparam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要修改之影像集的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 您要修改之影像集的操作框。 |
| setDefinition | `xsd:string` | 否 | 重設影像整合員。 |
| thumbAssetHandle | `xsd:string` | 否 | 資產的控制代碼，可作為影像集的縮圖。 |

**輸出(updateAssetSetReturn)**

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
