---
description: PropertySetType和createPropertySetTypeParam字段的有效值。
solution: Experience Manager
title: 属性集类型
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0c51e67-6927-4b9f-9935-222e6a194c13
TQID: 'https://experienceleague.adobe.com/yZz7rkrq0rzrrmSH-Wmza-LFExg23GcBp9MKc25wcrE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 5%

---

# [!DNL PropertySetType]{#propertysettype}

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 键入句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">公司句柄。 <p>注意：如果公司句柄不存在，则类型为全局。 </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 键入名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3">属性集类型之一。 请参阅输入(<span class="codeph"> createPropertySetTypeParam</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 是否允许将多个属性集实例附加到此类型的对象。 </td> 
  </tr> 
 </tbody> 
</table>

