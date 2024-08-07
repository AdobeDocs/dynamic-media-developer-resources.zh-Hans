---
description: 返回包含指定Photoshop路径的四边形坐标。
solution: Experience Manager
title: getPhotoshopPath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 46d88547-bb60-4370-9c79-bd281b40ba28
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 17%

---

# getPhotoshopPath{#getphotoshoppath}

返回包含指定Photoshop路径的四边形坐标。

语法

## 授权用户类型 {#section-c417a287612847cb98dd0aa9c67fd78a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 参数 {#section-ebffe496284c4ced9f329f78127be199}

**输入(getPhotoshopPathParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 用您要使用的映像处理公司。 |
| assetHandle | `xsd:string` | 是 | 处理图像资源。 |
| pathName | `xsd:string` | 是 | 要返回的Photoshop路径的名称。 |

**输出(getPhotoshopPathReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 透视图 | `types:PerspectiveQuad` | 是 | 基于路径返回图像坐标。 请参阅[透视四方](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)。 |

## 示例 {#section-1f0461cbdc184c8d8925336d5279db47}

**请求**

```java
<getPhotoshopPathParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
  <pathName>Face Path</pathName>
</getPhotoshopPathParam>
```

**响应**

```java
<getPhotoshopPathReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <perspectiveQuad>
    <x0>932.19</x0>
    <y0>296.592</y0>
    <x1>968.769</x1>
    <y1>320.16</y1>
    <x2>1119.56</x2>
    <y2>1200.0</y2>
    <x3>900.43</x3>
    <y3>1200.0</y3>
  </perspectiveQuad>
</getPhotoshopPathReturn>
```

>[!MORELIKETHIS]
>
>* [透视四方](../../../types/c-data-types/r-perspective-quad.md#reference-3c1f780f9c264e5b870b1ade24566204)
