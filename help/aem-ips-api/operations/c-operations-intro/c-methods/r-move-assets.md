---
description: 相互独立地移动多个资产。 它使用assetMoveArray中包含的AssetMove类型完成此操作。 每个AssetMove字段都包含一个目标文件夹。
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 12%

---

# moveAssets{#moveassets}

相互独立地移动多个资产。 它使用assetMoveArray中包含的AssetMove类型完成此操作。 每个AssetMove字段都包含一个目标文件夹。

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
| `*`companyHandle`*` | `xsd:string` | 是 | 要移动资产的公司的句柄。 |
| `*`assetMoveArray`*` | `types:AssetMoveArray` | 是 | 资产移动数组。 它包含资产和资产目标文件夹。 |

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 已成功移动资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 操作尝试移动时生成警告的资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 操作尝试移动时生成错误的资产计数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> </span>AssetOperationFaults，其中包含： 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">发出警告的资产。 </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">警告代码。 </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">警告的原因。 </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 类型：AssetOperationFaultArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <span class="codeph"> </span>AssetOperationFaults，其中包含： 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">导致错误的资产。 </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">错误代码。 </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">错误的原因。 </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## 示例 {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

此代码示例会将资产移动到`assetMoveArray`指定的特定位置。 数组包括资产句柄及其文件夹句柄。 响应指示资产已成功移动。

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
