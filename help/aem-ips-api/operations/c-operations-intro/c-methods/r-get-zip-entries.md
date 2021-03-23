---
description: 返回Zip文件数据。
seo-description: 返回Zip文件数据。
seo-title: getZipEntries
solution: Experience Manager
title: getZipEntries
uuid: cfc45f83-1cf9-4c50-9aac-5a731e62a839
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 19%

---


# getZipEntries{#getzipentries}

返回Zip文件数据。

语法

## 授权用户类型{#section-33a3f03ba8a14086922397619ce12ab8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-aa3f498fe76d4a5f99c42d64520fadce}

**输入(getZipEntriesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含Zip文件的公司的句柄。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 处理Zip文件。 |

**输出(getZipEntriesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`zipArray`*` | `types:ZipEntryArray` | 是 | Zip文件中的条目数组。 |

## 示例 {#section-1fc0ad8fa448492cb5a135d3e3d161ac}

此代码示例返回Zip文件信息，包括压缩和未压缩大小。

**请求**

```java
<getZipEntriesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetHandle>a|94223|27|30602</assetHandle>
</getZipEntriesParam>
```

**响应**

```java
<getZipEntriesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <zipArray
      <items>
         <name>Checklist_Images/.DS_Store</name>
         <isDirectory>false</isDirectory>
         <lastModified>2007-05-09T15:41:52.000-07:00</lastModified>
         <compressedSize>503</compressedSize>
         <uncompressedSize>6148</uncompressedSize>
      </items>
   ...
   </zipArray>
</getZipEntriesReturn>
```

