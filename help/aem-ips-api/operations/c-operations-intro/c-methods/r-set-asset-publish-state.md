---
description: 确定资产是否已准备好发布。
seo-description: 确定资产是否已准备好发布。
seo-title: setAssetPublishState
solution: Experience Manager
title: setAssetPublishState
topic: Dynamic Media Image Production System API
uuid: b7d49d77-573c-4e2a-81d3-196c09d62853
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 18%

---


# setAssetPublishState{#setassetpublishstate}

确定资产是否已准备好发布。

语法

## 授权用户类型{#section-11bec77e50b24461bb8c8aacf016eec8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读写权限。

## 参数 {#section-09d2ba001a2a455a9102550272f3eecb}

**输入(setAssetPublishStateParam)**

<table id="table_23CB72BFB8984CDF82D7207E7D82FC43"> 
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
   <td colname="col4"> 公司的把手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 资产句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">可用状态： 
    <ul id="ul_A2614608DF1E4DB6BF8141D33E59D180"> 
     <li id="li_8C90BFEEE2B14A0184F342018C45EE67"><span class="codeph"> MarkedForPublish</span> </li> 
     <li id="li_C4BC12B304DA4763956C3049AF597D06"><span class="codeph"> NotMarkedForPublish</span> </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代码短语  </span> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
  </tr> 
 </tbody> 
</table>

**输出**

IPS API不返回此操作的响应。

## 示例 {#section-c31ead6d0e594317a12c120509527792}

此代码示例使用`NotMarkedForPublish`设置资产的发布状态。

**请求**

```java
<setAssetPublishStateParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>24267|1|17063</assetHandle>
   <publishState>NotMarkedForPublish</publishState>
</setAssetPublishStateParam>
```

**响应**

无。
