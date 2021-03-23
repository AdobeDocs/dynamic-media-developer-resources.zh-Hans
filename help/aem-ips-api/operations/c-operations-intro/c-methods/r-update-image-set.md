---
description: 更新图像集。
seo-description: 更新图像集。
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 17%

---


# updateImageSet{#updateimageset}

更新图像集。

语法

## 参数 {#section-3be47dbbce474ce78676b05e163492e3}

**Input(updateImageSetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含要修改的图像集的公司的手柄。 |
| `*`assetHandle`*` | `xsd:string` | Ys | 要修改的图像集的手柄。 |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | 否 | 重置图像集成员。 |
| `*`thumbAssetHandle`*` | `xsd:string` | 否 | 用作图像集缩略图的资产手柄。 |

**输出(updateImageSetReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`序列`*` |  |  |  |

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

