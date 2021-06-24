---
description: 获取公司资产的原始文件路径。
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 15%

---

# getOriginalFilePaths{#getoriginalfilepaths}

获取公司资产的原始文件路径。

语法

## 授权用户类型 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要对资产具有读取访问权限。

## 参数 {#section-a6b394daba6e49a8882cf3051035d9d1}

**输入(getOriginalFilePathsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要获取其原始文件路径的资产的句柄数组。 |

**Output(getOriginalFilePathsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`originalFileArray`*` | `types:StringArray` | 是 | 表示原始文件路径的字符串数组。 |

## 示例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

此代码示例可返回使用资产句柄数组中的唯一资产句柄指定的资产的文件路径。

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
