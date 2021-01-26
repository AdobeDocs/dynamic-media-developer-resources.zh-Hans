---
description: 为现有标记字段设置标记字典值。
seo-description: 为现有标记字段设置标记字典值。
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Dynamic Media Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 15%

---


# setTagFieldValues{#settagfieldvalues}

为现有标记字段设置标记字典值。

语法

## 授权用户类型{#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-a05cbee4cb4f44198c414a6b14e69156}

**輸入**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 标记字段句柄。 |
| `*`valueArray`*` | `types:StringArray` | 是 | 替换字段现有词典的标记值的数组。 当新值与现有值匹配时，将保留资产关联。 |

**输出(setTagFieldValuesReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-b11cafd9bed54ab5836c737cc075c918}

**请求**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**响应**

无。
