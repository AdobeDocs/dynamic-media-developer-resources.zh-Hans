---
description: 使用公司的控制代碼和屬性集型別的名稱來取得屬性集型別。 它取得一個型別結構，其中包含型別的控制代碼以及屬性型別。
solution: Experience Manager
title: getPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ff9c3d24-577c-4a9c-8820-60c2a33773bc
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 11%

---

# getPropertySetType{#getpropertysettype}

使用公司的控制代碼和屬性集型別的名稱來取得屬性集型別。 它取得一個型別結構，其中包含型別的控制代碼以及屬性型別。

语法

## 授權的使用者型別 {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-c9a53400c44744668bd7915f72d2bf3d}

**輸入(getPropertySetTypeParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 否 | 公司的控制代碼。 選擇性，因為一個屬性集型別可以屬於多個公司。 |
| 名称 | `xsd:string` | 是 | 屬性集型別名稱。 |

**輸出(getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：PropertySetType</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">包含下列專案的型別結構： 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">控點。 </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">輸入名稱。 </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">屬性型別。 </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">表示型別是否允許多種屬性型別的值。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-1b57199415e34a8fa449f864f8895b14}

此程式碼範例會依名稱傳回屬性集型別。

**请求**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**响应**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```
