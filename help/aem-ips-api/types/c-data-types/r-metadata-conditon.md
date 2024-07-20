---
description: 添加用于searchAssets的搜索词。
solution: Experience Manager
title: 元数据条件
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 9226fb81-b3ff-41e4-a3cd-d5a40f359be6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '173'
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
