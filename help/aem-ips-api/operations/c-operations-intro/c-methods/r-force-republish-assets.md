---
description: 重置一个或多个资产的发布状态，以强制在下一个发布作业中重新发布资产。
seo-description: 重置一个或多个资产的发布状态，以强制在下一个发布作业中重新发布资产。
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Dynamic Media Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 11%

---


# forceRepublishAssets{#forcerepublishassets}

重置一个或多个资产的发布状态，以强制在下一个发布作业中重新发布资产。

语法

## 授权用户类型{#section-3d5a3e3afea748d69845de5c8c376448}

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
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>处理包含要重置的资产的公司。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> 重新发布文件</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定资产的文件将重新发布到投放服务器。 默认值为<span class="codeph"> true</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定用于服务资产的目录元数据已同步，以确保其为最新元数据。 此参数用于解决同一记录在接近并发更新时发生的竞争条件。 默认值为<span class="codeph"> false</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:HandleArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要重置发布状态的资产的句柄阵列。 </p> </td> 
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
   <td colname="col2"> <span class="codeph"> types:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>发布状态更新的阵列。 </p> </td> 
  </tr> 
 </tbody> 
</table>

