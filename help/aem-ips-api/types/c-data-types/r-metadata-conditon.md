---
description: 添加用于searchAssets的搜索词。
solution: Experience Manager
title: 元数据条件
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 9226fb81-b3ff-41e4-a3cd-d5a40f359be6
TQID: 'https://experienceleague.adobe.com/JcDip5MGpF6iPa1UqHZSe95h4G8lTjQycdBRaIny4N8'
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
source-wordcount: 171
ht-degree: 2%

---

# [!DNL MetadataCondition]{#metadatacondition}

添加用于searchAssets的搜索词。

语法

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
   <td colname="col3"> 字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">操作</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 字符串比较运算符的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 要测试的值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 布尔比较值（仅适用于布尔类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> 长比较值（仅适用于int类型的字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> 范围比较中的最小长值（仅适用于int类型的字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxLong</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：long</span> </td> 
   <td colname="col3"> 范围比较中的最大长值（仅适用于int类型的字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> 双精度比较值（仅适用于浮点类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> 范围比较中的最小双精度值（仅适用于浮点类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDouble</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：double</span> </td> 
   <td colname="col3"> 范围比较中的最大双精度值（仅适用于浮点型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">日期值</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 日期比较值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 范围比较中的最小日期值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDate</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：dateTime</span> </td> 
   <td colname="col3"> 范围比较中的最大日期值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">区分大小写</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> 确定元数据服务器区分大小写。 在<span class="codeph"> searchAssetsByMetadata</span>调用中使用。 </p> <p>请参阅<a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> searchAssetsByMetadata</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

