---
description: 執行特定工作。
solution: Experience Manager
title: executejob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4b2a2a14-d785-43bd-b1fc-2812d9f21964
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 21%

---

# executejob{#executejob}

執行特定工作。

语法

## 授權的使用者型別 {#section-8199e8599ea64e7097a2acb633417b15}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-2c61b2bffcf9479a9391f2c13fdf7d53}

**輸入(executeJobParam)**

<table id="table_FA410513908F4084A21A5F0A9431006C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>工作所屬公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> jobHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要執行之工作的控制代碼。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(executeJobReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-96f71aa58a954293b9a98ff96d86f232}

此程式碼範例會執行排定在IPS中執行的作業。

**请求**

```java
<executeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</executeJobParam>
```

**响应**

无。
