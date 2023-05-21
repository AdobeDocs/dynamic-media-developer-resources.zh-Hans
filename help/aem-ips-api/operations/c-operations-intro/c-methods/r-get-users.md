---
description: 取得公司、群組和使用者角色控制代碼所指定的使用者陣列。 此操作可讓您對傳回的使用者進行排序並按字元進行篩選。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 10%

---

# getUsers{#getusers}

取得公司、群組和使用者角色控制代碼所指定的使用者陣列。 此操作可讓您對傳回的使用者進行排序並按字元進行篩選。

## 授權的使用者型別 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| includeInactive | `xsd:boolean` | 否 | 包含或排除非作用中的使用者。 非IPS管理員使用者必須是至少一個公司的作用中成員，才能獲得授權進行任何API呼叫。 如果使用者沒有有效的公司成員資格，則會傳回授權錯誤。 |
| includeInvalid | `xsd:boolean` | 否 | 可讓您包含/排除無效的使用者。 |
| companyHandleArray | `types:HandleArray` | 否 | 依公司篩選結果。 |
| groupHandleArray | `types:HandleArray` | 否 | 依群組篩選結果。 |
| userRoleArray | `types:StringArray` | 否 | 依使用者角色篩選結果。 |
| charFilterField | `xsd:string` | 否 | 依欄位的字串首碼篩選結果(請參閱 [!DNL Trash State).] |
| charFilter | `xsd:string` | 否 | 依特定字元篩選結果。 |
| sortby | `xsd:string` | 否 | 使用者排序欄位的選擇。 |
| recordsPerPage | `xsd:int` | 否 | 傳回每頁的指定記錄數。 |
| resultsPage | `xsd:int` | 否 | 結果頁面。 |

**輸出(getUsersReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userArray | `types:UserArray` | 是 | 使用者陣列。 |

## 示例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

此程式碼範例會傳回多個選用引數的使用者陣列。 使用者角色、使用者字元篩選欄位和使用者排序欄位都是透過使用特定的字串常數來決定。

**请求**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**响应**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```
