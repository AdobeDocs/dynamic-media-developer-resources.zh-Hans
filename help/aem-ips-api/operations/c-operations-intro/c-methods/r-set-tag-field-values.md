---
description: 为现有标记字段设置标记词典值。
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 15%

---


# setTagFieldValues{#settagfieldvalues}

为现有标记字段设置标记词典值。

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
| `*`valueArray`*` | `types:StringArray` | 是 | 替换字段现有词典的标记值数组。 当新值与现有值匹配时，将维护资产关联。 |

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
