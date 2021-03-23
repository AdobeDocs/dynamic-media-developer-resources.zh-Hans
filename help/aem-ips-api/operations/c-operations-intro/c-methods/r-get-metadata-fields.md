---
description: 获取与资产关联的用户定义的元数据字段。
seo-description: 获取与资产关联的用户定义的元数据字段。
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
feature: Dynamic Media Classic，SDK/API，元数据
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 13%

---


# getMetadataFields{#getmetadatafields}

获取与资产关联的用户定义的元数据字段。

语法

## 授权用户类型{#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-bac949e59c0546429c5786fe422d750d}

**输入(getMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`assetType`*` | `xsd:string` | 是 | 要从中获取元数据的资产类型。 |

**输出(getMetadataFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`代码短语`*` | `Code Phrase` |  |  |

## 示例 {#section-dbfde1483d614b5aac2b491cb32115d7}

此代码示例返回指定类型和公司的元数据资产。 响应包含字段数组中的元数据字段数组。 并非所有资产都具有相同的元数据。 IPS用户定义资产的元数据字段。

**请求**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**响应**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

