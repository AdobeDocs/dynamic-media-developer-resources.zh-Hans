---
title: removeFolderPermissions
description: 删除文件夹权限。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 10830980-d504-4610-96c9-730937453256
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 18%

---

# removeFolderPermissions{#removefolderpermissions}

删除文件夹权限。

语法

## 授权用户类型 {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-7efa68377fd846219b906d354ae64ed3}

**输入(removeFolderPermissionsParam)**

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
   <td colname="col4"> 公司的句柄，该公司具有您要删除的权限文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 文件夹句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChilds</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>时间 <span class="codeph"> true</span>： 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">权限删除会传播到所有文件夹权限操作。 </li> 
     </ul> </p> <p>时间 <span class="codeph"> false</span>： 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">该操作仅影响指定的文件夹。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(removeFolderPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此代码示例从文件夹及其子文件夹中删除权限。 设置 `updateChildren` 到 `false` 仅从父文件夹中删除权限。

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
