---
description: 更新现有资源集的集定义。
solution: Experience Manager
title: setAssetSetDefinition
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f3fbe13b-e650-4a5d-9c46-a492b11fa13e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 5%

---

# setAssetSetDefinition{#setassetsetdefinition}

更新现有资源集的集定义。

语法

## 授权用户类型 {#section-9d4ca3a8cfe74934b89971de01a2143c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-c2057a5a13d042c684a3da1b49bc5dc6}

**输入(setAssetDefinitionParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 资产集所在公司的句柄。 |
| assetHandle | `xsd:string` | 是 | 资源集句柄 |
| setDefinition | `xsd:string` | 是 | 定义字符串。 请参阅下文。 |

**输出(setAssetSetDefinitionReturn)**

IPS API不返回此操作的响应。

## setDefinition参数：关于 {#section-f88e066bf5294b4f8c12d5d652a5c94c}

**setDefinition函数**

指定`setDefinition`内嵌替换函数。 这些将在目录查找期间或发布时解决。 替换字符串的格式为`${<substitution_func>}`，并且包括以下内容：

>[!NOTE]
>
>参数列表中的句柄文字必须用括号`([])`括起来。 在解析期间，替代字符串外部的文本将被复制到输出字符串。

<table id="table_A93D2C273B694C289208AA926B2597CD"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 替换函数 </th> 
   <th colname="col2" class="entry"> 返回资产的 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getFilePath([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 主文件路径。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getCatalogd([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目录ID。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getMetaData([ <span class="varname"> asset_handle </span>]，[ <span class="varname"> metadata_field_handle </span>]) </span> </td> 
   <td colname="col2"> 元数据值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> getThumbCatalogId([ <span class="varname"> asset_handle </span>]) </span> </td> 
   <td colname="col2"> 目录ID。 应用于基于图像的资产（图像、已调整视图、图层视图）。 <p>对于其他资产，返回缩略图资产的目录ID（如果有）。 如果没有缩略图资源与资源相关联，则函数返回空字符串。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**setDefinition示例**

此媒体集定义字符串：

```java
${getCatalogId([a|1664|22|1664])};${getCatalogId([a|1664|22|1664])}; 
1,${getFilePath([a|1036|19|144])};${getCatalogId([a|452|1|433])};2; 
${getMetadata([a|1036|19|144], [m|1|ASSET|SharedDateField])}
```

在查找或发布时解析为以下内容：

```java
jcompany/myRenderSet;jcompany/myRenderSet; 
1,jcompany/Videos/N08275_flv.flv;jcompany/myimg-1;2;20090703 10:05:53
```

## 示例 {#section-739b42eec3074cafae285ec015a2d088}

**请求**

```java
<setAssetSetDefinitionParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31"> 
   <companyHandle>c|1</companyHandle> 
   <assetHandle>a|1802|44|1802</assetHandle> 
   <setDefinition>${getCatalogId([a|1553|1|1176])};${getCatalogId([a|1553|1|1176])};1;img1, 
   ${getCatalogId([a|632|1|452])};${getCatalogId([a|632|1|452])};1,${getCatalogId([a|1664|22|1664])}; 
   ${getCatalogId([a|1664|22|1664])};1,${getFilePath([a|1036|19|144])};${getCatalogId([ a|452|1|433])}; 
   2;${getMetadata([a1036|19|144], [m|1|ASSET|SharedDateField])}</setDefinition> 
</setAssetSetDefinitionParam>
```

**响应**

无。
