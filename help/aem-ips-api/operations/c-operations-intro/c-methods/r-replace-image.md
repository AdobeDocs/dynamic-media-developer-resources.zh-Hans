---
description: 替换图像资产的图像数据。
solution: Experience Manager
title: replaceImage
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: bf8c1f5c-7829-4750-b5b7-b8b20d115d17
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 15%

---

# replaceImage{#replaceimage}

替换图像资产的图像数据。

语法

## 授权用户类型 {#section-e2aad71fb2a54612badc7b16f82ed544}

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
| `*`companyName`*` | `xsd:string` | 是 | 包含要替换的图像的公司句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 要替换的资产的句柄。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 生成新图像数据的图像服务器命令。 |

**输出(replaceImageReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 处理新资产。 |

## 示例 {#section-cebb93576bde4cb98cb27356ca66783b}

此代码示例替换了一个图像，并使用命令应用`urlModifier` ，该命令指定在替换时图像服务器将不采取任何操作。

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
