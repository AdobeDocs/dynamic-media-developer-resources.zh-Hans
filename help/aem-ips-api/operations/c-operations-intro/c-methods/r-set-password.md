---
description: 視您是否指定使用者控制代碼而定，將特定使用者或預設使用者的密碼設定為特定值。
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 7%

---

# setPassword{#setpassword}

視您是否指定使用者控制代碼而定，將特定使用者或預設使用者的密碼設定為特定值。

密碼到期日為選用。 如果省略，密碼將永不過期。

## 授權的使用者型別 {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*僅限* 此 `IpsAdmin` 使用者型別有權對其他使用者執行setPassword呼叫。

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## 参数 {#section-0531294341f7483d89dacaa393dd659a}

**輸入(setPasswordParam)**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>使用者控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 密碼 </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>密码. </p> <p>所選密碼上會強制執行下列要求： </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">密碼區分大小寫。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">密碼長度下限為8個字元。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">密碼必須包含下列字元類別中的一或多個字元： 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">小寫英文字元。 例如， <span class="codeph"> a b c d e </span> 等等 </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">大寫英文字元。 例如， <span class="codeph"> A B C D E </span> 等等。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">数量. 例如， <span class="codeph"> 1 2 3 4 5 </span> 等等。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊符號字元。 例如，您可以使用下列任何一項： <span class="codeph"> &amp;grave； ~ ！@ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ ： " ； ' &lt; &gt; ？， . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd：dateTime </span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>決定密碼到期日。 <p>注意：提供此欄位請求的時區。 時區會調整為中部時間。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(setPasswordReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-23a6fbabdb3c4c3180076057e47ae567}

此程式碼範例會建立使用者密碼。 密碼永不過期，因為 `passwordExpires` 省略。

**请求**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**响应**

无。
