---
description: searchAssets操作的系统字段搜索条件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

searchAssets操作的系统字段搜索条件。

对于一元比较，只传递一个值( `boolVal`， `longVal`， `doubleVal`，或 `dateVal`)，具体取决于系统字段类型。 对于搜索范围，通过 `min<Type>` 和 `max<Type>` 参数并传递 `op` 值 `Between` 或 `NotBetween`.

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 字段 | `xsd:string` | 资源搜索系统字段的选择。 |
| op | `xsd:string` | 字符串比较运算符的选择。 |
| 价值 | `xsd:string` | 要作为测试依据的值。 |
| 布尔值 | `xsd:boolean` | 布尔比较值。 |
| longVal | `xsd:long` | 长比较值。 |
| minLong | `xsd:long` | 长程下限。 |
| maxLong | `xsd:long` | 长范围的上限。 |
| 双精度值 | `xsd:double` | 双精度比较值。 |
| minDouble | `xsd:double` | 双范围下限。 |
| maxDouble | `xsd:double` | 双精度范围的上限。 |
| 日期值 | `xsd:dateTime` | 日期比较值。 |
| minDate | `xsd:dateTime` | 日期范围最小值。 |
| maxDate | `xsd:dateTime` | 日期范围最大值。 |

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
