---
description: 获取公司资源的原始文件路径。
seo-description: 获取公司资源的原始文件路径。
seo-title: getOriginalFilePaths
solution: Experience Manager
title: getOriginalFilePaths
topic: Scene7 Image Production System API
uuid: c4acf288-1a57-4295-806b-348f15a089cc
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 14%

---


# getOriginalFilePaths{#getoriginalfilepaths}

获取公司资源的原始文件路径。

语法

## 授权用户类型{#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要对资产具有读取权限。

## 参数 {#section-a6b394daba6e49a8882cf3051035d9d1}

**输入(getOriginalFilePathsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| ` *`assetHandleArray`*` | `types:HandleArray` | 是 | 要获取其原始文件路径的资源的句柄数组。 |

**输出(getOriginalFilePathsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`originalFileArray`*` | `types:StringArray` | 是 | 表示原始文件路径的字符串数组。 |

## 示例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

此代码示例返回资产句柄数组中使用唯一资产句柄指定的资产的文件路径。

**请求**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**响应**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```

