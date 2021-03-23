---
description: 删除资产的元数据值。 使用元数据删除的数组在批处理中设置值。
seo-description: 删除资产的元数据值。 使用元数据删除的数组在批处理中设置值。
seo-title: deleteAssetMetadata
solution: Experience Manager
title: deleteAssetMetadata
uuid: 2dc783c6-23da-4a94-8780-3c4ec88ff3f4
feature: Dynamic Media Classic，SDK/API，元数据，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---


# deleteAssetMetadata{#deleteassetmetadata}

删除资产的元数据值。 使用元数据删除的数组在批处理中设置值。

语法

## 授权用户类型{#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有资产的读取和删除权限。

## 参数 {#section-0eed164e278b456fbdfb7a50727a0416}

**输入(deleteAssetMetadataParam)**

<table id="table_A4438E2FE5F245E5B73F46CD887BE70F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名称 </p> </th> 
   <th colname="col2" class="entry"> <p>类型 </p> </th> 
   <th colname="col3" class="entry"> <p>必需 </p> </th> 
   <th colname="col4" class="entry"> <p>说明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>companyHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>文件夹所属公司的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>assetHandle </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要删除的资产的句柄。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>metadataDelete </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要从资产中删除的元数据。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>deleteArray </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 类型：MetadataDeleteArray</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>要从资产中删除的元数组。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**输出(deleteAssetMetadataParam)**

IPS API不返回此操作的响应。

## 示例 {#section-d5657289f5234bb0a613dcf691507958}

元数据删除

```java
    <complexType name="MetadataDelete">
        <sequence>
            <element name="fieldHandle" type="xsd:string"/>
        </sequence>
    </complexType>
```

示例调用

```java
<ac:Request id="deleteAssetMetadata">
 <deleteAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
  <companyHandle>c|101</companyHandle>
  <assetHandle>a|202</assetHandle>
  <deleteArray>
   <items>
    <fieldHandle>m|2919|ASSET|UntypedUDFField1395788289789</fieldHandle>
   </items>
  </deleteArray>
 </deleteAssetMetadataParam>
</ac:Request>
```

