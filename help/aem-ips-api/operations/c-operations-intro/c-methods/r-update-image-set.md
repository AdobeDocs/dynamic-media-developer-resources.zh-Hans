---
description: 更新影像集。
solution: Experience Manager
title: updateImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 20%

---

# updateImageSet{#updateimageset}

更新影像集。

语法

## 参数 {#section-3be47dbbce474ce78676b05e163492e3}

**輸入(updateImageSetparam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要修改之影像集的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 您要修改之影像集的操作框。 |
| memberArray | `types:ImageSetMemberUpdateArray` | 否 | 重設影像整合員。 |
| thumbAssetHandle | `xsd:string` | 否 | 資產的控制代碼，可作為影像集的縮圖。 |

**輸出(updateImageSetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 序列 |  |  |  |

## 示例 {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**请求**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**响应**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
