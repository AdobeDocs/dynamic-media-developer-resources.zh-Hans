---
description: 创建一个通用资产集，其中包含要发布到图像服务器的原始集定义字符串。
solution: Experience Manager
title: createAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 4565eb4f-eeb7-4b98-bfef-1a59e9a931af
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 10%

---

# createAssetSet{#createassetset}

创建一个通用资产集，其中包含要发布到图像服务器的原始集定义字符串。

语法

## 授权用户类型 {#section-d670d3af552147199b65c7eb847544a3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-3580b586296e42a5b21426085b1bb72d}

**输入(createAssetSet)**

<table id="table_2C70C33A127242FC828FCD8EC852E1EC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含资产集的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 创建新资产集的文件夹的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 资产名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> subType </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 客户端为资产集类型创建的唯一标识符。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> setDefinition </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 设置定义字符串中的参数。 <p>必须解析为目标查看器指定的格式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAssetHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用作新图像集缩略图的资产处理。 如果未指定，IPS会尝试使用该集引用的第一个图像资产。 </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition的替换函数**

您可以在行中指定在目录查找或发布期间解析的替换函数。 替换字符串的格式为 `${<substitution_func>}`. 下面枚举了可用函数。

>[!NOTE]
>
>参数列表中的句柄文字必须被括号括起来 `([])`. 在分辨率期间，替换字符串以外的所有文本都会逐字复制到输出字符串。

| **替换函数** | **返回结果** |
|---|---|
| `getFilePath([asset_handle>])` | 资产的主要源文件路径。 |
| `getCatalogId([<asset_handle>])` | 资产的目录ID。 |
| `getMetaData([<asset_handle>], [<metadata_field_handle>])` | 资产的元数据值。 |
| `getThumbCatalogId([<asset_handle>])` | 资产的目录ID（仅适用于基于图像的资产）。关联的缩略图资产的目录ID（适用于其他资产）。 如果关联的缩略图资产不可用，则函数会返回空字符串。 |

**示例媒体集定义字符串**

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|103 
6|19|144])};${getCatalogId([a|452|1|433])};2;${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])} 
```

在目录查找或发布时，它将解析为类似于以下内容的字符串：

```java
jcompany/myRenderSet;jcompany/myRenderSet;1,jcompany/Videos/Somebodys_N08275_flv.flv;jcomp any/myimg-1;2;20090703 10:05:53
```

**输出(createAssetSet)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 资产集的句柄。 |

## 示例 {#section-fed53089de824d67ab96cd9103d384b4}

**请求**

```java
<createAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <folderHandle>f|jcompany/AssetSets/</folderHandle> 
   <name>testAssetSet</name> 
   <subType>MediaSet</subType> 
</createAssetSetParam>
```

**响应**

```java
<createAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <assetHandle>a|1801|44|1801</assetHandle> 
</createAssetSetReturn>
```
