---
description: 取得陣列中的所有使用者。
solution: Experience Manager
title: getAllUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: db1fd5c9-80f5-463a-870f-be3e38c21bab
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 24%

---

# getAllUsers{#getallusers}

取得陣列中的所有使用者。

语法

## 授權的使用者型別 {#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-f092ca72f2024d66a1cec690aeab870a}

**輸入(getAllUsersParam)**

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">設定為： 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108"><span class="codeph"> true</span> 以包含無效的使用者。 </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> false</span> 以忽略無效的使用者。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAllUsersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userArray | `types:UserArray` | 是 | 所有使用者的陣列。 |
| 程式碼片語 | `Code Phrase` |  |  |

## 示例 {#section-9c9a2d335513478da20652c1b1443731}

此程式碼範例會傳回所有使用者。 為簡短起見，回應會遭截斷。

**请求**

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**响应**

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```
