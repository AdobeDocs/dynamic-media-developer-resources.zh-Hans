---
description: 設定現有標籤欄位的標籤字典值。
solution: Experience Manager
title: settagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 17%

---

# settagFieldValues{#settagfieldvalues}

設定現有標籤欄位的標籤字典值。

语法

## 授權的使用者型別 {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-a05cbee4cb4f44198c414a6b14e69156}

**輸入**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| fieldHandle | `xsd:string` | 是 | 標籤欄位控制代碼。 |
| valueArray | `types:StringArray` | 是 | 取代欄位現有字典的標籤值陣列。 當新值與現有值相符時，會維護資產關聯。 |

**輸出(setTagFieldValuesReturn)**

IPS API未傳回此作業的回應。

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
