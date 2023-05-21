---
description: 取得與指定資產相關聯的資產以及與其關係的詳細資訊。
solution: Experience Manager
title: getAssociatedAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: cf49719f-5d79-4e64-a785-bf3b2fe200c7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '407'
ht-degree: 8%

---

# getAssociatedAssets{#getassociatedassets}

取得與指定資產相關聯的資產以及與其關係的詳細資訊。

语法

## 授權的使用者型別 {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-d11d0dab59e94e89b466123a0ebfa82e}

**輸入(getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
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
   <td colname="col4"> <p>處理擁有資產的公司。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>資產控點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>所需的回應欄位陣列。 請參閱簡介中的response- FieldArray/excludeFieldArray 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 型別：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>排除的回應欄位陣列。 請參閱簡介中的response- FieldArray/excludeFieldArray 。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> containerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>包含指定資產的集合與範本資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定集或範本資產所包含的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerReferenceArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>圖層或範本URL中參照的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ownerArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>擁有指定資產的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用來產生指定資產的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatorarray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>此 <span class="codeph"> generatorarray</span> 列出建立此資產的方式。 例如，如果 <span class="codeph"> assetHandler</span> 是PDF的影像頁面，則其中會包含PDF處理器工具並參照PdfFile資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>此 <span class="codeph"> generatedArray</span> 反轉建立此資產的方式。 例如， <span class="codeph"> generatedArray</span> 可以包含由此產生的影像清單 <span class="codeph"> assetHandler</span> 如果這是Pdf檔案資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 型別：資產</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與請求資產相關聯的縮圖資產資訊。 如果未指派縮圖資產，回應中會忽略欄位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以使用引數 `responseFieldArray` 或 `excludeFieldArray` 以限制回應大小。 尤其是 `GenerationInfo` 專案傳回 `generatorArray` 或 `generatedArray` 預設為同時包含建立者和產生的資產記錄。 對於PDF資產型別，此行為會在回應中導致不需要的「創作者」PDF資產記錄多個副本。 您可以透過新增以下專案來消除此問題 `generatedArray/items/originator` 至 `excludeFieldArray`. 或者，您可以指定要加入的明確回應欄位清單 `responseFieldArray`.

## 示例 {#section-8946ea4b9cb94912a8408249c897f192}

以下基本範例是為從PDF擷取的影像要求產生器的控制代碼。 它包含 `containerArray` 長度為1，且專案包含 `assetHandle` PDF的。

**请求**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**响应**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

上述範例的相反情況如下：

**请求**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**响应**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

在下個範例中，群組會新增至公司，具有 `groupHandleArray`. 此範例僅使用一個群組。

**请求**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**响应**

无。
