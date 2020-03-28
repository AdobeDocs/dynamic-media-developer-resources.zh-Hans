---
description: 分别移动多个资产。 它使用assetMoveArray中包含的AssetMove类型来实现此操作。 每个AssetMove字段都包含一个目标文件夹。
seo-description: 分别移动多个资产。 它使用assetMoveArray中包含的AssetMove类型来实现此操作。 每个AssetMove字段都包含一个目标文件夹。
seo-title: moveAssets
solution: Experience Manager
title: moveAssets
topic: Scene7 Image Production System API
uuid: 178f9979-fff5-45ce-a001-1263d1770ea8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAssets{#moveassets}

分别移动多个资产。 它使用assetMoveArray中包含的AssetMove类型来实现此操作。 每个AssetMove字段都包含一个目标文件夹。

语法

## 授权用户类型 {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7d47f663474b41cc83439288ac133cc5}

**输入(moveAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 要移动的资产所在公司的处理。 |
| ` *`assetMoveArray`*` | `types:AssetMoveArray` | 是 | 资产移动阵列。 它包含一个资产和一个资产目标文件夹。 |

**输出(moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> 成 <span class="varname"> 功计数</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 已成功移动资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 操作尝试移动时生成警告的资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> error <span class="varname"> Count</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 操作尝试移动时生成错误的资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> warningDetailArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> 包</span>含以下项的AssetOperationFaults: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">引发警告的资产。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告代码。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告的理由。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> errorDetailArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> 包</span>含以下项的AssetOperationFaults: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">引发错误的资源。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">错误代码。 </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">错误原因。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

此代码示例将资产移动到由指定的特定位置 `assetMoveArray`。 数组包括资产句柄及其文件夹句柄。 响应表示资产已成功移动。

**请求**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**响应**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

