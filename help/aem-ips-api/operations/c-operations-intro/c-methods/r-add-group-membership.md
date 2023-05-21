---
description: 將使用者新增至群組陣列。
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 14%

---

# addGroupMembership{#addgroupmembership}

將使用者新增至群組陣列。

语法

## 授權的使用者型別 {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-e250f6ddb13646808c6a8860b6442bc5}

**輸入(addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>處理您要新增其群組成員資格的使用者。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>您希望公司所屬的群組的控制代碼陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(addGroupMembershipParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-f7a1f40c3d7a40ea964b29056c734d81}

此範例會將群組新增至具有groupHandleArray的公司。 此範例僅使用一個群組。

**请求**

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**响应**

无。
