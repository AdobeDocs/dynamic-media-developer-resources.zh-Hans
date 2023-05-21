---
description: 取得唯一的中繼資料欄位值。
solution: Experience Manager
title: getUniqueMetadataValues
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: ac5f5667-6c94-425c-bc01-f9df48d16e00
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 28%

---

# getUniqueMetadataValues{#getuniquemetadatavalues}

取得唯一的中繼資料欄位值。

语法

## 授權的使用者型別 {#section-6a6b67e10a4c4e7bb18306115713380e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-b9d1413811c24566b6d095701f0f66db}

**輸入(getUniqueMetadataValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| fieldHandle | `xsd:string` | 否 | 中繼資料欄位的控點。 |

**輸出(getUniqueMetadataValuesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 值 | `type:StringArray` |  |  |

## 示例 {#section-440f3bc3e5be436cb6ec26117d05f476}

此程式碼範例使用欄位控制代碼來傳回特定的中繼資料值。

**请求**

```java
<ns1:getUniqueMetadataValuesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
</ns1:getUniqueMetadataValuesParam>
```

**响应**

```java
<getUniqueMetadataValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <values>
      <items>320</items>
   </values>
</getUniqueMetadataValuesReturn>
```
