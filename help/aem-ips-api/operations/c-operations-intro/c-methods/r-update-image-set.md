---
description: 更新图像集。
solution: Experience Manager
title: 更新图像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: d8d5fb80-17f1-424f-8a61-27189f87d603
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 17%

---

# 更新图像集{#updateimageset}

更新图像集。

语法

## 参数 {#section-3be47dbbce474ce78676b05e163492e3}

**输入(updateImageSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要修改的图像集的公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 要修改的图像集的句柄。 |
| memberArray | `types:ImageSetMemberUpdateArray` | 否 | 重置图像集成员。 |
| thumbAssetHandle | `xsd:string` | 否 | 充当图像集缩略图的资产句柄。 |

**输出(updateImageSetReturn)**

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
