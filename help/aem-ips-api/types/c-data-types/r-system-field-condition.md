---
description: searchAssets操作的系统字段搜索条件。
seo-description: searchAssets操作的系统字段搜索条件。
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets操作的系统字段搜索条件。

对于一元比较，请根据系统字段类型仅传递一个值（`boolVal`、`longVal`、`doubleVal`或`dateVal`）。 对于搜索范围，传递`min<Type>`和`max<Type>`参数并传递`op`值`Between`或`NotBetween`。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`字段`*` | `xsd:string` | 资产搜索系统字段的选择。 |
| `*`op`*` | `xsd:string` | 字符串比较运算符的选择。 |
| `*`值`*` | `xsd:string` | 要测试的值。 |
| `*`boolVal`*` | `xsd:boolean` | 布尔值比较值。 |
| `*`longVal`*` | `xsd:long` | 比较值较长。 |
| `*`minLong`*` | `xsd:long` | 长程的下边界。 |
| `*`maxLong`*` | `xsd:long` | 长程的上边界。 |
| `*`doubleVal`*` | `xsd:double` | 多次比较值。 |
| `*`minDouble`*` | `xsd:double` | 多次范围的下边界。 |
| `*`maxDouble`*` | `xsd:double` | 多次范围的上边界。 |
| `*`dateVal`*` | `xsd:dateTime` | 日期比较值。 |
| `*`minDate`*` | `xsd:dateTime` | 日期范围最小。 |
| `*`maxDate`*` | `xsd:dateTime` | 日期范围最大值。 |

## 示例 {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

