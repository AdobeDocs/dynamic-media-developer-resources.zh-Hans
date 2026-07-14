---
title: 元数据字段
description: 特定资源的用户定义的字段定义。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 97175076-9078-4bc4-b3ea-73c3ea772f6a
TQID: 'https://experienceleague.adobe.com/8BYmsgczpTi43XrDRYL8lEkaKfKvrLbAteGG8euPweE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 2%

---

# [!DNL MetadataField]{#metadatafield}

特定资源的用户定义的字段定义。

使用`getMetadataFields`或`getAssetMetadataField`操作检索标记字段定义。

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
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 元数据字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 元数据字段名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">类型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 元数据字段类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 元数据字段的默认值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isRequired</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 设置所需的状态。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isUserDefined</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 确定元数据字段是否由用户定义。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3">隐藏或公开IPS系统特定的元数据。 从<a href="../../operations/c-operations-intro/c-methods/r-get-metadata-fields.md#reference-170337127801401d9ea54bd4ccf28efe" format="dita" scope="local"> getMetadataFields</a>和<a href="../../operations/c-operations-intro/c-methods/r-get-asset-metadata-fields.md#reference-ea57f8e98d3e443da66114550b0d0a28" format="dita" scope="local"> getAssetMetadataFields</a>返回。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">是强制的</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> <p>布尔标记，指示在设置值时是否强制（验证）元数据字段类型。 </p> <p>如果设置为true，则如果在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中设置非法值，则会引发错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 通过此选项可创建一组选定的标记可指向的共享指定值。 </td> 
  </tr> 
 </tbody> 
</table>

