---
description: 更新字段元数据。
seo-description: 更新字段元数据。
seo-title: updateMetadataField
solution: Experience Manager
title: updateMetadataField
topic: Dynamic Media Image Production System API
uuid: 8712b09b-b02a-4fb3-a0ed-084dc48a717a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 21%

---


# updateMetadataField{#updatemetadatafield}

更新字段元数据。

语法

## 授权用户类型{#section-540e91823fee49a4920ca738f7bfeb99}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-69681ed1ddff437ca1c73f46fe835c96}

**输入(updateMetadataFieldParam)**

<table id="table_65D6EE6C402E4F01819822A855B6BB7F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 参数名称 </th> 
   <th colname="col2" class="entry"> 类型 </th> 
   <th colname="col3" class="entry"> 必需 </th> 
   <th colname="col4" class="entry"> 说明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 公司手柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 元数据字段句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 元数据字段名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 元数据字段值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隐藏或公开IPS系统特定的元数据。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforced</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>一个布尔标志，指示设置值时是否强制（验证）元数据字段。 </p> <p>如果设置为true，则如果在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中设置了非法值，则会引发错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 允许您创建选定标记可以指向的一组共享枚举值。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(updateMetadataFieldReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | 是 | 元数据字段句柄。 |

## 示例 {#section-bb7d93ab6d914ddfa294e08983e589ee}

此代码示例更新为元数据字段分配新名称和默认值。 响应将返回更新字段的句柄。

**请求**

```java
<updateMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
   <name>updateMetadataField</name>
   <defaultValue>Default</defaultValue>
</updateMetadataFieldParam>
```

**响应**

```java
<updateMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|updateMetadataField</fieldHandle>
</updateMetadataFieldReturn>
```

