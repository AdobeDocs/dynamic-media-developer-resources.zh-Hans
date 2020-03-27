---
description: 删除多个资产。
seo-description: 删除多个资产。
seo-title: deleteAssets
solution: Experience Manager
title: deleteAssets
topic: Scene7 Image Production System API
uuid: ed446ebf-4a3d-4ee8-9ab3-596b1f05e5f4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deleteAssets{#deleteassets}

删除多个资产。

语法

## 授权用户类型 {#section-a6bc555b8ac840c98835b73fbf838d70}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4dc888e77d974ac794b553616dd11e86}

**输入(deleteAssetsParam)**

<table id="table_AAA6845769DB4B129C8A660D0CBA348A"> 
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
   <td colname="col4"> <p>资产所属公司的处理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> assetHandleArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:HandleArray</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要删除的资产数组。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(deleteAssetsParam)**

<table id="table_0C6D8D51A79248ACA2022DBB754A9B9C"> 
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
   <td colname="col1"> <p><span class="codeph"> 成 <span class="varname"> 功计数</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>已成功删除的资产数。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> warningCount</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>在操作尝试删除资产时生成警告的资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> error <span class="varname"> Count</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:int</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>在操作尝试删除时生成错误的资产。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> warningDetailArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>与资产关联的详细信息数组，当操作尝试删除资产时，这些资产会生成警告。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> errorDetailArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> types:AssetOperationFaultArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>与资产关联的详细信息数组，该资产在操作尝试删除资产时生成错误。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-aaad1933bf86479eb6cb476cec7d4587}

此代码示例向Web服务服务器发送请求中的公司和一组资 `deleteAssetsParam` 产句柄。 `deleteAssetsReturn` 返回成功计数2，表示两个资产均已删除。

**请求**

```java
<deleteAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</deleteAssetsParam>
```

**响应**

```java
<deleteAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</deleteAssetsReturn>
```

