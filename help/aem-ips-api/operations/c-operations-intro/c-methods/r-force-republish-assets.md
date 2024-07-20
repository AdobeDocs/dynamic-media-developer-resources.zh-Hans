---
description: 重置一个或多个资源的发布状态，以强制在下一次发布作业中重新发布该资源。
solution: Experience Manager
title: Forcerepublishassets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 9%

---

# Forcerepublishassets{#forcerepublishassets}

重置一个或多个资源的发布状态，以强制在下一次发布作业中重新发布该资源。

语法

## 授权用户类型 {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**输入(forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>包含要重置的资产的公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname">重新发布文件</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定将资产的文件重新发布到投放服务器。 默认为<span class="codeph"> true</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定用于提供资源的目录元数据已同步，以确保其为最新版本。 此参数用于解决几乎同时更新同一记录时可能发生的争用情况。 默认为<span class="codeph"> false</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>发布状态将被重置的资产句柄数组。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>发布状态更新的数组。 </p> </td> 
  </tr> 
 </tbody> 
</table>
