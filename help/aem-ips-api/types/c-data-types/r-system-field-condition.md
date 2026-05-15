---
description: searchAssets操作的系统字段搜索条件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 6%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

searchAssets操作的系统字段搜索条件。

对于一元比较，根据系统字段类型，只传递一个值（`boolVal`、`longVal`、`doubleVal`或`dateVal`）。 对于搜索范围，传递`min<Type>`和`max<Type>`参数并传递`Between`或`NotBetween`的`op`值。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 欄位 | `xsd:string` | 选择资产搜索系统字段。 |
| 操作 | `xsd:string` | 字符串比较运算符的选择。 |
| 价值 | `xsd:string` | 要测试的值。 |
| boolVal | `xsd:boolean` | 布尔比较值。 |
| longVal | `xsd:long` | 长比较值。 |
| minLong | `xsd:long` | 长范围下限。 |
| maxLong | `xsd:long` | 长范围的上限。 |
| doubleVal | `xsd:double` | 双精度比较值。 |
| minDouble | `xsd:double` | 双范围下限。 |
| maxDouble | `xsd:double` | 双精度范围的上限。 |
| 日期值 | `xsd:dateTime` | 日期比较值。 |
| minDate | `xsd:dateTime` | 日期范围最小值。 |
| maxDate | `xsd:dateTime` | 日期范围最大值。 |

## 示例： {#section-347d4aabfff44530adba03d1dc0b9968}

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
