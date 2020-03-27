---
description: 获取与指定资产关联的资产以及有关其关系的详细信息。
seo-description: 获取与指定资产关联的资产以及有关其关系的详细信息。
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

获取与指定资产关联的资产以及有关其关系的详细信息。

语法

## 授权用户类型 {#section-453cc706400345778713cda249bfac16}

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

**输入(getAssociatedAssetsParam)**

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
   <td colname="col1"> <p><span class="codeph"> 公司 <span class="varname"> 句柄</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>处理拥有该资产的公司。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 资 <span class="varname"> 产句柄</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>资产句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>所需的响应字段的数组。 请参阅“简介”中的response- FieldArray/excludeFieldArray。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> excludeFieldArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>被排除的响应字段的数组。 请参阅“简介”中的response- FieldArray/excludeFieldArray。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(getAssociatedAssetsReturn)**

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
   <td colname="col1"> <span class="codeph"> 容 <span class="varname"> 器阵列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>包含指定资产的集和模板资产的数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>由指定集或模板资产包含的资产数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> layerReferenceArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>图层或模板URL中引用的资产数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ownerArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>拥有指定资产的资产组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> derivedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用于生成指定资产的资产数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> generatorArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>generatorArray <span class="codeph"></span> 列表此资产的创建方式。 例如，如果 <span class="codeph"> assetHandler</span> 是PDF的图像页，则它将包含PDF处理器工具并引用PdfFile资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>生成的 <span class="codeph"> Array</span> 会反转创建此资产的方式。 例如，如果生 <span class="codeph"> 成的数组是PdfFile资源</span> ，则它可以包含从此assetHandler生成的 <span class="codeph"> 图像的列表</span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 缩略图资产</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：资产</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>与请求资产关联的缩略图资产信息。 如果未分配缩略图资产，则响应中将忽略该字段。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可以使用参数 `responseFieldArray` 或限 `excludeFieldArray` 制响应大小。 特别是，返回的 `GenerationInfo` 项目在默认 `generatorArray` 或默认 `generatedArray` 情况下包括原始和生成的资产记录。 对于PDF资产类型，此行为会在响应中导致“原创者”PDF资产记录的多个多余副本。 您可以通过添加到来消除此 `generatedArray/items/originator` 问题 `excludeFieldArray`。 或者，您可以指定要包含在其中的响应字段的显式列表 `responseFieldArray`。

## 示例 {#section-8946ea4b9cb94912a8408249c897f192}

以下基本示例是对从PDF中提取的图像的生成器句柄的请求。 它包含一 `containerArray` 个长度，其中包含一个包含PDF `assetHandle` 的项目。

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

上述示例的相反情况如下：

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

在下一个示例中，将组添加到具有的公司 `groupHandleArray`。 此示例仅使用一个组。

**请求**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**响应**

无。
