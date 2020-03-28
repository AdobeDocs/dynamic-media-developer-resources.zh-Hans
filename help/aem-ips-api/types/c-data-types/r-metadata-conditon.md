---
description: 添加搜索词以与searchAssets一起使用。
seo-description: 添加搜索词以与searchAssets一起使用。
seo-title: MetadataCondition
solution: Experience Manager
title: MetadataCondition
topic: Scene7 Image Production System API
uuid: 9d65b8ce-86a5-4730-af84-a87134fd7db6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataCondition{#metadatacondition}

添加搜索词以与searchAssets一起使用。

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
   <td colname="col1"> <span class="codeph"> 字 <span class="varname"> 段句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 字符串比较运算符的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 值</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 要测试的值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Boolean比较值（仅适用于Boolean类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> long Val</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 长比较值（仅适用于int-typed字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 最长</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 范围比较中的最小长值（仅限int-typed字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxLong</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> 范围比较中的最大长值（仅适用于int-typed字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3"> 多次比较值（仅适用于浮点型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 小双</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3"> 范围比较中的最小多次值（仅适用于浮点型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDouble</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:多次</span> </td> 
   <td colname="col3"> 范围比较中的最大多次值（仅适用于浮点型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateVale</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 日期比较值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 最 <span class="varname"> 小日期</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 范围比较中的最小日期值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 范围比较中的最大日期值（仅适用于日期类型字段）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 区分大小写 <span class="varname"></span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> 为元数据服务器建立区分大小写的设置。 在searchAssetsByMetadata调 <span class="codeph"> 用中使用</span> 。 </p> <p>请参 <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> 阅searchAssetsByMetadata</a>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

