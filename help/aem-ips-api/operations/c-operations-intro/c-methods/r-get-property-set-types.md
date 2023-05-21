---
description: 取得與指定公司相關聯的屬性集型別，或取得全域屬性集型別（若未指定公司）。
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 15%

---

# getPropertySetTypes{#getpropertysettypes}

取得與指定公司相關聯的屬性集型別，或取得全域屬性集型別（若未指定公司）。

语法

## 授權的使用者型別 {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-ac3ed9e036b54ea993f544046ff0e15d}

**輸入(getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">與屬性集型別相關聯之公司的控制代碼。 <p>如果您要傳回全域屬性集型別，請省略。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getPropertySetTypesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| typeArray | `types:PropertySetTypeArray` | 是 | 與指定公司關聯的屬性集型別陣列，如果未指定公司，則為全域屬性集型別。 |

## 示例 {#section-280c406a90864409856aee44d4069a52}

**请求**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**响应**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```
