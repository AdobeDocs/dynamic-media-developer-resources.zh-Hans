---
description: 返回给定图像的Photoshop路径名称数组。
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 19%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

返回给定图像的Photoshop路径名称数组。

语法

## 授权用户类型 {#section-baa0fd4b92bc4ad89809efd659b3a629}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 对包含要处理的图像的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理图像资产。 |

**Output(getPhotoshopPathNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | 是 | 图像中的Photoshop路径名称数组。 |

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
