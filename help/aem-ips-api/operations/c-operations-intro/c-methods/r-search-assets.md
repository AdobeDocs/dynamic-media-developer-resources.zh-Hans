---
description: 根据您指定的条件搜索资产。
seo-description: 根据您指定的条件搜索资产。
seo-title: searchAssets
solution: Experience Manager
title: searchAssets
topic: Scene7 Image Production System API
uuid: 125e9e0d-1856-4e80-9778-ca93cd04b766
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# searchAssets{#searchassets}

根据您指定的条件搜索资产。

语法

## searchAssets:关于 {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` 是检索IPS资源的主要方法。 此方法用于多种用途，如浏览文件夹层次结构或按名称查找特定资产。

**响应大小**

`searchAssets` 在一次电话联系中最多可返回1000个资产。 要在每次调用中返回最多10,000个资源，请将响应数据限制为、、、 `totalRows`、和字 `name`段的子 `handle``type``subType` 集。 要返回较大的集，请使用参数设置分 `resultPage` 页。

**使用responseFieldArray或excludeFieldArray限制结果文件大小**

使用或参数限制数据集 `responseFieldArray` 的大 `excludFieldArray` 小。 这些参数有助于减少内存使用和带宽，并可以缩短服务器响应时间。

## 授权用户类型 {#section-9c4bc41bb8b4493982197eb13c7cdc55}

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
>用户必须具有读取权限才能返回资产。

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
   <td colname="col1"> <span class="codeph"> 公司 <span class="varname"> 句柄</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含要搜索的资产的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允许管理员以其他用户的身份工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允许管理员作为其他组的一部分工作。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文 <span class="varname"> 件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 用于搜索资产的根路径。 如果省略，则使用公司根文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 包含子 <span class="varname"> 文件夹</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">设置为 <span class="codeph"> true</span> ，可搜索子文件夹。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 发布状态选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 垃圾 <span class="varname"> 状态</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">垃圾状态选择。 默认为 <span class="codeph"> NotInTrash</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> conditionMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>选择搜索匹配模式以组合关键字数组 <span class="codeph"> 的结果</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span>, and <span class="codeph"> metadataConditionArray</span>。 默认为“全 <span class="codeph"> 部匹配</span>”。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 关 <span class="varname"> 键字Array</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p> <p>注意： 已弃用参数。 建议您不要使用它。 </p> </p> <p>要匹配的关键字字符串数组。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> systemFieldMatchMode <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>选择“搜索匹配模式”以组合 <span class="codeph"> systemFieldCondition匹配</span> 。 默认为“全部匹 <span class="codeph"> 配”</span> </p>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> systemFieldConditionArray <span class="varname"></span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 系统字段条件的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 标 <span class="varname"> 记MatchMode</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式字符串常量。 默认值为 <span class="codeph"> MatchAll</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> tagConditionArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:TagConditionArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>标记字段搜索谓词的数组。 </p> <p>谓词根据标签MatchMode <span class="codeph"> 设置组合，然后与</span> keywordArray <span class="codeph"> 、</span>systemFieldConditionArray <span class="codeph"> 、</span><span class="codeph"></span><span class="codeph"></span> systemConditionArray和元数据中的任何术语组合，这些元数据根据条件MatchMode设置的JaximeSynchrode来组合。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 元 <span class="varname"> 数据MatchMode</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">搜索匹配模式以组合元数 <span class="codeph"> 据条件</span> 匹配。 默认为“全 <span class="codeph"> 部匹配</span>”。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 元 <span class="varname"> 数据条件数组</span></span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 元数据字段搜索条件的数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要包含在搜索中的资产类型阵列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要从搜索中排除的资产类型数组。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要筛选的子类型名称列表。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> strictSubType <span class="varname"> 检查</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">如 <span class="codeph"> 果为true</span> , <span class="codeph"> 且assetSubTypeArray不为空，则仅返回其子类型位于assetSubTypeArray中的</span> 资产 <span class="codeph"></span> 。 如果 <span class="codeph"> 为false</span> （默认），则返回未定义子类型的资产。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 排 <span class="varname"> 除副产品</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 如果为true，则在获取主资产（如翻录的PDF页面图像）期间生成的副产品资产将从搜索结果中排除。 默认值为 false。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludInbuslareArray</span></span> </td> 
   <td colname="col2"> <p> <span class="codeph"> types:ExcludeInsublareArray</span> </p> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 要从搜索结果中排除的副产品资产生成条件的数组。 如果存在，此参数将覆盖excludeInsproductes设置。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 项 <span class="varname"> 目处理</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sting</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 处理包含要搜索的资产的项目。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 每 <span class="varname"> 页记录</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 返回的最大结果数。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 结 <span class="varname"> 果页</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">根据recordsPerPage页面大小指定要返回的 <span class="codeph"> 结果页</span> 。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 排序方式</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 资产排序字段的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 排序方向的选择。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含一列表字段和子字段，以包含在响应中。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> excludeFieldArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> types:StringArray</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 包含一列表字段和子字段，以排除在响应之外。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(searchAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`totalRows`*` | `xsd:int` | 否 | 当每页记录数不限时，搜索返回的行数。 |
| ` *`assetArray`*` | `types:AssetArray` | 否 | 搜索返回的资产。 |

## 示例 {#section-725484cc09b54772a838ad2cc930b94b}

此代码示例搜索属于特定公司的图像资产。 响应被截断以简化。

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

