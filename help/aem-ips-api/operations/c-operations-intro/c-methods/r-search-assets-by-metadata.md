---
description: 搜尋指定搜尋詞的中繼資料索引儲存區域。 傳回資產資料，如searchAssets方法。
solution: Experience Manager
title: searchAssetsByMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: a0e01edb-c52b-436d-a166-e24cc6861c49
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 11%

---

# searchAssetsByMetadata{#searchassetsbymetadata}

搜尋指定搜尋詞的中繼資料索引儲存區域。 傳回資產資料，如searchAssets方法。

當 `searchAssetsByMetadata` 可讓您根據使用者定義的中繼資料欄位進行搜尋，若在中指定這些欄位，則不會傳回這些欄位 `responseMetadataArray`. 為了說明這一點，以下程式碼範例將說明這一點：

```java
<ns:responseMetadataArray>
 <ns:items>custom_attributes.x</ns:items>
</ns:responseMetadataArray>
```

傳回null值：

```java
<items>
 <name>custom_attributes.x</name>
 <value>null</value>
</items>
```

若要解決此問題，您可以使用 `fieldHandles` 從搜尋傳回要執行的資產的 `getAssets` (另請參閱 [getAssets](../../../operations/c-operations-intro/c-methods/r-get-assets.md#reference-adad4f504f684d3dabc09e093b8511ca))。 此方法會取得相關資產的使用者定義欄位值。 使用下列語法範例來搜尋使用者定義的中繼資料欄位：

```java
<ns:metadataConditionArray>
 <ns:items>
  <ns:fieldHandle>custom_attributes.[UDF Field Name]</ns:fieldHandle>
  <ns:op>[Conditional]</ns:op>
  <ns:value>[Value]</ns:value>
 </ns:items>
</ns:metadataConditionArray>
```

## 授權的使用者型別 {#section-9f85dd55ab574104b5fdc0f95aa0a0e2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-5f1edb9c5b914160ab361f4364b8aa8d}

**輸入(searchAssetsByMetadataParam)**

<table id="table_8FF228D6279241849F3D9E5BA080580C"> 
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
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>公司的控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> 篩選</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type：SearchFilter</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>可協助您定義搜尋條件的篩選器。 </p> <p>另請參閱 <a href="../../../types/c-data-types/r-search-filter.md#reference-0e2eb87bccae4b69be6717267bcb80aa" format="dita" scope="local"> SearchFilter</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>定義搜尋條件的條件。 如需詳細資訊，請參閱下文。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> responseMetadataArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> type：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>您要在資產摘要的回應中填入的其他欄位。 欄位必須以標準化格式指定。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>回應傳回的資產數量。 預設值為 1000。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定要傳回的結果頁面，根據 <span class="codeph"> recordsPerPage</span> 頁面大小。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sortby</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>依選取的資產欄位排序。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> sortDirection</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>選擇排序方向。 預設值為升序。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(searchAssetsByMetadataReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| totalRows | `xsd:int` | 否 | 相符專案的數量。 |
| assetArray | `types:AssetArray` | 否 | 搜尋傳回的資產陣列。 |

## metadataConditionArray詳細資料 {#section-1af4a4a22f82451eabdf6dfe13d9f27d}

**專案結構**

`metadataConditionArray` 結構如下：

```java
<ns1:items>
   <ns:fieldHandle>field_handle</ns:fieldHandle>
   <ns:op>operator</ns:op>
   <ns:value>comparison_value</ns:value>
</ms1:items>
```

**值**

`field_handle` 是中繼資料搜尋索引鍵。 其中可包含點標籤法。 可能的值包括：

* `asset_id` （沒有前置詞）
* `name`
* `folder_path`
* `type`
* `file_name`
* `description`
* `comment`
* `user_data`
* `sku`
* `modified_at`
* `modified_by`
* `created_at` (與 `modified_at` (日期格式： 2014年7月25日星期五22:13:45 GMT-0500 （中部夏令時間）

* `created_by`

**允許的運運算元**

此 [!DNL operator] 定義如何比較值並包含：

* `Equals`
* `NotEquals`
* `Contains`
* `NotContains`
* `StartsWith`
* `EndsWith`

此 `comparison_value` 是要搜尋的字詞。

## 示例 {#section-53a12b9c023e4e629eddf5719c955ad4}

此程式碼範例會使用下列中繼資料條件來執行搜尋：

* `name` 欄位包含 `1000801`.

* `dc.rights` 欄位等於 `Per Jessen Schmidt`.

**请求**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"
xmlns:xsd="http://www.scene7.com/IpsApi/xsd"
xmlns:ns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <soapenv:Header>
      <xsd:authHeader>
          <xsd:user>user@adobe.com</xsd:user>
          <xsd:password>topSecret</xsd:password>
      </xsd:authHeader>
   </soapenv:Header>
   <soapenv:Body>
      <ns:searchAssetsByMetadataParam>
         <ns:companyHandle>c|656</ns:companyHandle>
         <ns:metadataConditionArray>
            <ns:items>
               <ns:fieldHandle>name</ns:fieldHandle>
               <ns:op>Contains</ns:op>
               <ns:value>1000801</ns:value>
            </ns:items>
            <ns:items>
               <ns:fieldHandle>dc.rights</ns:fieldHandle>
               <ns:op>Equals</ns:op>
               <ns:value>Per Jessen Schmidt</ns:value>
            </ns:items>
         </ns:metadataConditionArray>
         <ns:responseMetadataArray>
            <ns:items>dc.subject</ns:items>
            <ns:items>xmp.CreatorTool</ns:items>
         </ns:responseMetadataArray>
      </ns:searchAssetsByMetadataParam>
   </soapenv:Body>
</soapenv:Envelope>
```

**响应**

```java
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/">
   <soapenv:Body>
      <searchAssetsByMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
         <totalRows>1</totalRows>
         <assetSummaryArray>
            <items>
               <assetHandle>a|885289</assetHandle>
               <type>Image</type>
               <name>test9-1000801</name>
               <folder>Extroscope/Test subfolders/</folder>
               <filename>test9-1000801.jpg</filename>
               <created>2009-11-19T07:21:24.252-08:00</created>
               <createUser>pschmidt@adobe.com</createUser>
               <lastModified>2009-11-19T07:21:25.487-08:00</lastModified>
               <lastModifyUser>pschmidt@adobe.com</lastModifyUser>
               <metadataArray>
                  <items>
                     <name>dc.subject</name>
                     <value>[San Fransico, USA</value>
                  </items>
                  <items>
                     <name>xmp.CreatorTool</name>
                     <value>Ver.1.0</value>
                  </items>
               </metadataArray>
            </items>
         </assetSummaryArray>
      </searchAssetsByMetadataReturn>
   </soapenv:Body>
</soapenv:Envelope>
```
