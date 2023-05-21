---
description: 取得與資產相關聯的使用者定義中繼資料欄位。
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 15%

---

# getMetadataFields{#getmetadatafields}

取得與資產相關聯的使用者定義中繼資料欄位。

语法

## 授權的使用者型別 {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-bac949e59c0546429c5786fe422d750d}

**輸入(getMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司控點。 |
| assetType | `xsd:string` | 是 | 從中取得中繼資料的資產型別。 |

**輸出(getMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 程式碼片語 | `Code Phrase` |  |  |

## 示例 {#section-dbfde1483d614b5aac2b491cb32115d7}

此程式碼範例會傳回指定型別和公司的中繼資料資產。 回應包含欄位陣列中的中繼資料欄位陣列。 並非所有資產都有相同的中繼資料。 ips使用者會定義資產的中繼資料欄位。

**请求**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**响应**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```
