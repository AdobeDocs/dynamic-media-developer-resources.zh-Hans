---
description: 根据资源名称数组返回资源。
solution: Experience Manager
title: getAssetsByName
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e48574e3-9d16-45fb-b4c8-98b5e092e611
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 10%

---

# getAssetsByName{#getassetsbyname}

根据资源名称数组返回资源。

语法

## 授权用户类型 {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>仅返回用户具有读取权限的资源。

## 参数 {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**输入(getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司的把手。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 提供作为其他用户的访问权限。 仅供管理员使用。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用于按特定组进行筛选。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 要检索的资源名称数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 对于检索到的资源，允许资源类型数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 为检索到的资源排除的资源类型数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 对于检索到的资源，允许资源子类型数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>如果<span class="codeph"> true</span>和<span class="codeph"> assetSubTypeArray</span>不为空，则只返回子类型位于<span class="codeph"> assetSubTypeArray</span>中的资产。 </p> <p>如果<span class="codeph"> false</span>，则包含未定义子类型的资源。 </p> <p>默认值为<span class="codeph"> false</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含响应中包含的字段和子字段列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph">类型：StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含从响应中排除的字段和子字段的列表。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(getAssetsByNameReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetArray | `types:AssetArray` | 否 | 与筛选条件匹配的资源数组。 |

## 示例 {#section-3b7447398e574c88aeaf8ca159cc78dd}

此代码示例返回两个图像类型资产。

**请求**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**响应**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```
