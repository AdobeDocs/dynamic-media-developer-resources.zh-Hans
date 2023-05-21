---
description: 從IPS傳回資產。
solution: Experience Manager
title: getAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 3b63da9c-f10a-40bf-8e3c-4f0bfc53d74c
source-git-commit: e7370f699fea8a2c248a33ebc8925d98231e6b26
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 21%

---

# getAssets{#getassets}

從IPS傳回資產。

语法

## 授權的使用者型別 {#section-4673c1c9f4314160af8b165eb2dd20cc}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>僅傳回使用者有權存取的資產。

## 参数 {#section-bb9cf1ab19ea47acbd9ae58646dbe273}

**輸入(getAssetsParam)**

<table id="table_15CDEFC7F836411C80AA122E3A701C77"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>模擬特定使用者。 僅供管理員使用。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>按组过滤. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd：HandleArray</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>根資料夾，可擷取葉層級的資料夾和所有子資料夾。 如果排除，則使用公司根目錄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>回應中包含的欄位和子欄位。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：StringArray</span> </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p>從回應中排除的欄位和子欄位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAssetsReturn)**

<table id="table_694932BBBD2C4167871380B2CF514BEA"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：AssetArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>符合篩選條件的資產陣列。 </p> </td> 
  </tr> 
 </tbody> 
</table>
