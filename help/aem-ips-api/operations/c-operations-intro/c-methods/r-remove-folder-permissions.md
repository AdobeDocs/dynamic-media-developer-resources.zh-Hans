---
description: 删除文件夹权限。
seo-description: 删除文件夹权限。
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
topic: Scene7 Image Production System API
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
   <td colname="col1"> <span class="codeph"> 公司 <span class="varname"> 句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 具有您要删除的权限的文件夹的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文件 <span class="varname"> 夹处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 处理文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 更 <span class="varname"> 新子项</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>如果 <span class="codeph"> 为真</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">删除权限会传播到所有文件夹权限操作。 </li> 
     </ul> </p> <p>如果 <span class="codeph"> 为false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">此操作仅影响指定的文件夹。 </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(removeFolderPermissionsReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-04390f0ec7cc460cb5d34d518e33e7a5}

此代码示例从文件夹及其子文件夹中删除权限。 如果 `updateChildren` 您只 `false` 需要从父级文件夹删除权限，请设置为。

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
