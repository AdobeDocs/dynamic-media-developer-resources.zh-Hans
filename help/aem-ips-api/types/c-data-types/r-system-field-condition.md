---
description: searchAssets作業的系統欄位搜尋條件。
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

searchAssets作業的系統欄位搜尋條件。

若要進行一元比較，請只傳遞一個值( `boolVal`， `longVal`， `doubleVal`，或 `dateVal`)視系統欄位型別而定。 如需搜尋範圍，請通過 `min<Type>` 和 `max<Type>` 引數並傳遞 `op` 值 `Between` 或 `NotBetween`.

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 字段 | `xsd:string` | 資產搜尋系統欄位的選擇。 |
| op | `xsd:string` | 字串比較運運算元的選擇。 |
| 价值 | `xsd:string` | 要測試的值。 |
| 布林值 | `xsd:boolean` | 布林值比較值。 |
| longVal | `xsd:long` | 長比較值。 |
| minLong | `xsd:long` | 長範圍的下限。 |
| maxLong | `xsd:long` | 長範圍的上限。 |
| doubleval | `xsd:double` | 雙精度比較值。 |
| minDouble | `xsd:double` | 雙精度範圍下限。 |
| maxDouble | `xsd:double` | 雙精度範圍的上限。 |
| 日期值 | `xsd:dateTime` | 日期比較值。 |
| minDate | `xsd:dateTime` | 日期範圍下限。 |
| maxDate | `xsd:dateTime` | 日期範圍上限。 |

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
