---
description: 移除檔案夾許可權。
solution: Experience Manager
title: removeFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 17%

---

# removeFolderPermissions{#removefolderpermissions}

移除檔案夾許可權。

语法

## 授權的使用者型別 {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-7efa68377fd846219b906d354ae64ed3}

**輸入(removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 具有您要移除之許可權資料夾的公司控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 資料夾的控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChilds</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>時間 <span class="codeph"> true</span>： 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">許可權移除會傳播到所有檔案夾許可權操作。 </li> 
     </ul> </p> <p>時間 <span class="codeph"> false</span>： 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">此操作只會影響指定的資料夾。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(removeFolderPermissionsReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此程式碼範例會從資料夾及其子資料夾中移除許可權。 設定 `updateChildren` 至 `false` 如果您只需要從父資料夾中移除許可權。

**请求**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**响应**

无。
