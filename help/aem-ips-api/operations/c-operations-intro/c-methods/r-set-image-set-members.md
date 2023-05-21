---
description: 設定與影像集相關聯的資產清單。
solution: Experience Manager
title: setImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 12%

---

# setImageSetMember{#setimagesetmembers}

設定與影像集相關聯的資產清單。

此操作會忽略 `pageReset` 的引數 `ImageSets` 和 `SpinSets` 和會強制將值設為true。

## 授權的使用者型別 {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有影像集資產的讀取和寫入存取權，以及每個成員資產的讀取存取權。

## 参数 {#section-2f46efcd24c648aeacba738509426e46}

**輸入(setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col4"> <p>公司控點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像集控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 屬於影像集的資產成員陣列。 </td> 
  </tr> 
 </tbody> 
</table>

**輸出(setImageSetMembersReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-7b87219034464aa98524178ccee27738}

此程式碼範例使用成員陣列來設定影像集的成員。

**请求**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**响应**

无。
