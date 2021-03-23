---
description: 获取为一个或多个标签字段定义的所有标签词典值。
seo-description: 获取为一个或多个标签字段定义的所有标签词典值。
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 15%

---


# getTagFieldValues{#gettagfieldvalues}

获取为一个或多个标签字段定义的所有标签词典值。

语法

## 授权用户类型{#section-cc36a437394c491594e704a08a161c87}

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

**输入(getTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含标签字段的公司的句柄。 |
| `*`fieldHandleArray`*` | `types:HandleArray` | 是 | 要返回的标记值的字段句柄数组。 |

**输出(getTagFieldValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`fieldArray`*` | `types:TagFieldValuesArray` | 是 | 字典中每个请求字段的标记值的数组。 |

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

