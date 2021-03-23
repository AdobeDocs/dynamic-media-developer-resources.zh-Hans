---
description: 根据您指定的条件搜索资产。
seo-description: 根据您指定的条件搜索资产。
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 12%

---


# searchAssets{#searchassets}

根据您指定的条件搜索资产。

语法

## searchAssets:关于{#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` 是检索IPS资源的主要方法。此方法用于多种用途，如浏览文件夹层次结构或按名称查找特定资产。

**响应大小**

`searchAssets` 在一次电话联系中最多返回1000个资产。要在每次调用中返回多达10,000个资源，请将响应数据限制为`totalRows`、`name`、`handle`、`type`和`subType`字段的子集。 要返回较大的集，请使用`resultPage`参数设置分页。

**使用responseFieldArray或excludeFieldArray限制结果文件大小**

使用`responseFieldArray`或`excludFieldArray`参数限制数据集的大小。 这些参数有助于减少内存使用和带宽，并可缩短服务器响应时间。

## 授权用户类型{#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有返回资产的读取权限。

## 参数 {#section-49aabc0600764f55a8b7017d86ded44f}

**输入(searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需? </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 您要搜索的资产的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允许管理员以其他用户的身份工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允许管理员作为其他组的一部分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 文件夹</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用于搜索资产的根路径。 如果省略，则使用公司根文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">设置为<span class="codeph"> true</span>可搜索子文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 发布状态选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">垃圾状态选择。 默认值为<span class="codeph"> NotInTrash</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>用于组合<span class="codeph">关键字数组</span>、 </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray和</span>metadataConditionArray <span class="codeph"> 中</span>。默认值为<span class="codeph"> MatchAll</span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> <p>注意： 已弃用参数。 建议您不要使用它。 </p> </p> <p>要匹配的关键字字符串数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>用于组合<span class="codeph"> systemFieldCondition</span>匹配的搜索匹配模式选择。 默认值为<span class="codeph"> MatchAll</span> </p>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 系统字段条件的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式字符串常量。 默认值为<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagConditionArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>标记字段搜索谓词的数组。 </p> <p>谓词根据<span class="codeph"> tagMatchMode</span>设置进行组合，然后根据<span class="codeph"> conditionMatch条件与<span class="codeph"> keywordArray</span>、<span class="codeph"> systemFieldConditionArray</span>和<span class="codeph"> metadataConditionArray</span>中的任意项进行组合Mode</span>设置。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式以组合<span class="codeph"> metadataCondition</span>匹配。 默认值为<span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> 类型：MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 元数据字段搜索条件的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要包含在搜索中的资产类型的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要从搜索中排除的资产类型的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要筛选的子类型名称列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> strictSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">如果<span class="codeph"> true</span>和<span class="codeph"> assetSubTypeArray</span>不为空，则只返回子类型位于<span class="codeph"> assetSubTypeArray</span>中的资产。 如果<span class="codeph"> false</span>（默认），则返回未定义子类型的资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeInsproductes</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 如果为true，则在获取主资产（如翻录的PDF页面图像）期间生成的副产品资产将从搜索结果中排除。 默认值为 false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludBybsuleArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeBybsuleArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要从搜索结果中排除的副产品资产生成条件的数组。 如果存在，此参数将覆盖excludeInspluments设置。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 处理包含要搜索的资产的项目。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要返回的最大结果数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultsPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">根据<span class="codeph"> recordsPerPage</span>页面大小指定要返回的结果页面。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 资源排序字段的选项。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 排序方向的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要包含在响应中的字段和子字段的列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含要从响应中排除的字段和子字段的列表。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(searchAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | 否 | 当每页记录数不限时，搜索返回的行数。 |
| `*`assetArray`*` | `types:AssetArray` | 否 | 搜索返回的资产。 |

## 示例 {#section-725484cc09b54772a838ad2cc930b94b}

此代码示例搜索属于特定公司的图像资产。 响应被截断以便简短。

**请求**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**响应**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

