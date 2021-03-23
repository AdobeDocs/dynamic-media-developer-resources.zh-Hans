---
description: 允许管理员创建新的元数据字段以与内容管理系统协调或用于模板操作。 创建的元数据字段的示例包括关键字、有关图像作者的信息或版权持有人信息。
seo-description: 允许管理员创建新的元数据字段以与内容管理系统协调或用于模板操作。 创建的元数据字段的示例包括关键字、有关图像作者的信息或版权持有人信息。
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 12%

---


# createMetadataField{#createmetadatafield}

允许管理员创建新的元数据字段以与内容管理系统协调或用于模板操作。 创建的元数据字段的示例包括关键字、有关图像作者的信息或版权持有人信息。

语法

## 授权用户类型{#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## 参数 {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**输入(createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 元数据字段所属公司的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 资源类型. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 要创建的元数据字段的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">元数据字段类型。 <p>元数据字段类型常量定义可用类型。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>要创建的元数据字段的默认值（例如，<span class="codeph"> Scene 7</span>）。 </p> <p>标记字段类型不支持默认值，必须忽略默认值。 如果为标记字段类型指定了非空默认值，则将返回错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隐藏或公开特定于IPS系统的元数据。 </td> 
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
   <td colname="col4"> 允许您创建选定标记可指向的一组共享枚举值。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(createMetadataFieldReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | 是 | 新元数据字段的句柄。 |

## 示例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

此代码示例创建名为`createMetadataField`的字符串类型元数据字段。 响应将返回新元数据字段的句柄。

**请求**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**响应**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

