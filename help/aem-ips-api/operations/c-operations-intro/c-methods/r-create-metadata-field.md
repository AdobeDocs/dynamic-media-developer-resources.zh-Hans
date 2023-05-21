---
description: 可讓管理員建立新的中繼資料欄位，以協調內容管理系統或範本操作。 建立的中繼資料欄位範例包括關鍵字、影像作者的相關資訊或版權持有人資訊。
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 13%

---

# createMetadataField{#createmetadatafield}

可讓管理員建立新的中繼資料欄位，以協調內容管理系統或範本操作。 建立的中繼資料欄位範例包括關鍵字、影像作者的相關資訊或版權持有人資訊。

语法

## 授權的使用者型別 {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## 参数 {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**輸入(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 引數名稱 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 中繼資料欄位所屬的公司名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 资源类型. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 您正在建立的中繼資料欄位名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">中繼資料欄位型別。 <p>中繼資料欄位型別常數會定義可用的型別。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 預設值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>要建立的中繼資料欄位的預設值(例如， <span class="codeph"> Scene 7</span>)。 </p> <p>標籤欄位型別不支援預設值，必須省略。 如果為標籤欄位型別指定了非空白的預設值，則會傳回錯誤。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ishidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隱藏或公開IPS系統特定的中繼資料。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>布林值標幟，指出在設定值時，是否強制執行（驗證）中繼資料欄位。 </p> <p>若設為true，則若在中設定了不合法的值，則會擲回錯誤 <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTag值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 可讓您建立一組所選標籤可指向的共用列舉值。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(createMetadataFieldReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| fieldHandle | `xsd:string` | 是 | 新中繼資料欄位的控制代碼。 |

## 示例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

此程式碼範例會建立字串型別中繼資料欄位，稱為 `createMetadataField`. 回應會傳回新中繼資料欄位的控制代碼。

**请求**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**响应**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```
