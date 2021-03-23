---
description: 返回给定图像的Photoshop路径名数组。
seo-description: 返回给定图像的Photoshop路径名数组。
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 16%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

返回给定图像的Photoshop路径名数组。

语法

## 授权用户类型{#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-605a4aab23104489a21f7f7f5849801b}

**输入(getPhotoshopPathNamesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 处理包含要处理的图像的公司。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理图像资产。 |

**输出(getPhotoshopPathNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | 是 | 图像中的Photoshop路径名数组。 |

## 示例 {#section-6d316f14b4184d42af4ca3f717b042dd}

**请求**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**响应**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

