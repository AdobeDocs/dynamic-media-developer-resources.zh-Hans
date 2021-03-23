---
description: 替换图像资产的图像数据。
seo-description: 替换图像资产的图像数据。
seo-title: replaceImage
solution: Experience Manager
title: replaceImage
uuid: 46824e33-265c-4425-9ab1-8ad6b7ac154d
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 14%

---


# replaceImage{#replaceimage}

替换图像资产的图像数据。

语法

## 授权用户类型{#section-e2aad71fb2a54612badc7b16f82ed544}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-0d0ab668fa6d4310a93fb7ef8d8dd1e0}

**Input(replaceImageParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 要替换的图像的公司的手柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要替换的资产的句柄。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 生成新图像数据的图像服务器命令。 |

**输出(replaceImageReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 处理新资产。 |

## 示例 {#section-cebb93576bde4cb98cb27356ca66783b}

此代码示例替换一个图像，并使用一个命令应用`urlModifier`，该命令指定图像服务器在替换时不会采取任何操作。

**请求**

```java
<replaceImageParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|140626|1|102524</assetHandle>
   <urlModifier>action=none</urlModifier>
</replaceImageParam>
```

**响应**

```java
<replaceImageReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|140626|1|102524</assetHandle>
</replaceImageReturn>
```

