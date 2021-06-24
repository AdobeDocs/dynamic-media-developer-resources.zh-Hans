---
description: 通过比较资产名称与公司的图像提供/图像呈现目录命名空间中的所有名称，检查IPS ID冲突。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# checkAssetNames{#checkassetnames}

通过比较资产名称与公司的图像提供/图像呈现目录命名空间中的所有名称，检查IPS ID冲突。

语法

## 授权用户类型 {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 参数 {#section-9c75b00f2072453abea0bdefc6ad7c99}

**输入(checkAssetNamesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 包含用户的公司的句柄。 |
| `*`assetNamesArray`*` | `types:StringArray` | 是 | 要检查的资产名称数组。 |

**输出(checkAssetNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | 是 | 正在使用的资产名称数组。 |

## 示例 {#section-bc5d120d74614a63a425ca3acc337219}

此示例代码会请求指定公司正在使用的资产名称。 响应会返回一个正在使用的资产名称数组。

**请求**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**响应**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
