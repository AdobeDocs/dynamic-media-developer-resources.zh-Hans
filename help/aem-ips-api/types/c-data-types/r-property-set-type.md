---
description: PropertySetType和createPropertySetTypeParam字段的有效值。
seo-description: PropertySetType和createPropertySetTypeParam字段的有效值。
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Scene7 Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# PropertySetType{#propertysettype}

PropertySetType和createPropertySetTypeParam字段的有效值。

值包括：

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 键入handle。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 公司 <span class="varname"> 句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">公司手柄。 <p>注意： 如果公司手柄不存在，则类型为全局。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 键入名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 属 <span class="varname"> 性类型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">属性集类型之一。 请参阅输入(<span class="codeph"> createPropertySetTypeParam</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 允 <span class="varname"> 许多个</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 是否允许将多个属性集实例附加到此类型的对象。 </td> 
  </tr> 
 </tbody> 
</table>

