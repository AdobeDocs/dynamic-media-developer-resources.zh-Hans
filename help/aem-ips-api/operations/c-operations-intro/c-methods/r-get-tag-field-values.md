---
description: 获取为一个或多个标记字段定义的所有标记字典值。
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 17%

---

# getTagFieldValues{#gettagfieldvalues}

获取为一个或多个标记字段定义的所有标记字典值。

语法

## 授权用户类型 {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input(getTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含标记字段的公司的句柄。 |
| `*`fieldHandleArray`*` | `types:HandleArray` | 是 | 要返回的标记值的字段句柄数组。 |

**Output(getTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | 是 | 字典中每个请求字段的标记值数组。 |

## 示例 {#section-4492742614e44bb191a7d397dc1a1407}

**请求**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**响应**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
