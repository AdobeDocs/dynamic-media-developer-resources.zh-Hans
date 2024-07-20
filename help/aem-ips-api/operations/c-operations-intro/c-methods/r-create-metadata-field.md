---
title: createMetadataField
description: 它允许管理员创建元数据字段以协调内容管理系统或模板操作。 创建的元数据字段的示例包括关键字、有关图像作者的信息或版权持有人信息。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: eac7fa54-ebe2-4f42-a478-d9a6fb54d1b6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 6%

---

# createMetadataField{#createmetadatafield}

它允许管理员创建元数据字段以协调内容管理系统或模板操作。 创建的元数据字段的示例包括关键字、有关图像作者的信息或版权持有人信息。

语法

## 授权用户类型 {#section-2f61d79f8cac4692bfa53b95035ddd89}

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
   <td colname="col1"> <span class="codeph"> <span class="varname">公司名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 元数据字段所属公司的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">资产类型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 资源类型。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname">名称</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 正在创建的元数据字段的名称。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4">元数据字段类型。 <p>元数据字段类型常量定义可用的类型。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> <p>要创建的元数据字段的默认值（例如，<span class="codeph">场景7</span>）。 </p> <p>标记字段类型不支持默认值，必须省略。 如果为标记字段类型指定了非空默认值，则会返回错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 隐藏或公开IPS系统特定的元数据。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname">是强制的</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd：boolean</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>布尔标记，指示在设置值时是否强制（验证）元数据字段。 </p> <p>如果设置为true，则如果在<span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>中设置非法值，则会引发错误。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 通过此选项可创建一组选定的标记可指向的共享特定值。 </td> 
  </tr> 
 </tbody> 
</table>

**输出(createMetadataFieldReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| fieldHandle | `xsd:string` | 是 | 新元数据字段的句柄。 |

## 示例 {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

此代码示例创建一个名为`createMetadataField`的字符串类型元数据字段。 响应将返回新元数据字段的句柄。

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
