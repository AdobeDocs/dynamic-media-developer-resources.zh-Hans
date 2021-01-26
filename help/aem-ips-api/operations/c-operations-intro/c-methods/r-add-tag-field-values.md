---
description: 向现有标记字段的字典添加新标记值。
solution: Experience Manager
title: addTagFieldValues
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---


# addTagFieldValues{#addtagfieldvalues}

向现有标记字段的字典添加新标记值。

语法

## 授权用户类型{#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**输入(addTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含标记字段的公司的句柄。 |
| `*`fieldHandle`*` | `xsd:string` | 是 | 要修改的标记字段的句柄。 |
| `*`valueArray`*` | `xsd:string` | 是 | 要添加到字段现有词典的标记值的数组。 |

**输出(addTagFieldValuesParam)**

IPS API不返回此操作的响应。

## 示例 {#section-c4049392f1c548f883b8b1f8f167bada}

**请求**

```java
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**响应**

无。
