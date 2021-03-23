---
description: 为与setAssetMetadata一起使用的特定资产设置元数据值。 描述您要对元数据所做的更改。
seo-description: 为与setAssetMetadata一起使用的特定资产设置元数据值。 描述您要对元数据所做的更改。
seo-title: 元数据更新
solution: Experience Manager
title: 元数据更新
uuid: 09d3940b-117d-4d83-8b12-e86520c9da34
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 4%

---


# MetadataUpdate{#metadataupdate}

为与setAssetMetadata一起使用的特定资产设置元数据值。 描述您要对元数据所做的更改。

>[!NOTE]
>
>如果传递了单个值字段，则资产的标记值将重置为指定的标记值。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 元数据字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 元数据更新值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Boolean元数据值（仅用于Boolean类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 长元数据值（仅适用于int-typed字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3"> 多次元数据值（仅适用于浮动类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日期元数据值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> addTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> <p>添加到资产的现有标记值列表。 
     <ul id="ul_08DE6C490B614560A6118E7AC59720E3"> 
      <li id="li_358A3BDC0EC94CCF8178CD789F09F804">单值标记字段仅存储最后一个值。 </li> 
      <li id="li_3F47D3A3C63A4752BF9A45F7B00A6E70">如果值不在词典中，则固定词典标记字段返回错误。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3">替换资产的现有标记值列表。 
    <ul id="ul_941C915C69E84CF2AC5938378837EB92"> 
     <li id="li_6E85019335034B2EB1302696AE690ED5">单值标记字段仅存储最后一个值。 </li> 
     <li id="li_0DC56717EBB642D29FB7A3D043CEDED1">如果值不在词典中，则固定词典标记字段返回错误。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> deleteTagValueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 从资产的标记值列表（如果存在）中删除指定的值。 </td> 
  </tr> 
 </tbody> 
</table>

