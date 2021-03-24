---
description: 通过将资源名称与公司的图像服务/图像渲染目录命名空间中的所有名称进行比较，检查IPS ID冲突。
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 12%

---


# checkAssetNames{#checkassetnames}

通过将资源名称与公司的图像服务/图像渲染目录命名空间中的所有名称进行比较，检查IPS ID冲突。

语法

## 授权用户类型{#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## 参数{#section-9c75b00f2072453abea0bdefc6ad7c99}

**输入(checkAssetNamesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 否 | 包含用户的公司的句柄。 |
| `*`assetNamesArray`*` | `types:StringArray` | 是 | 要检查的资源名称数组。 |

**输出(checkAssetNamesReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | 是 | 正在使用的资源名称数组。 |

## 示例 {#section-bc5d120d74614a63a425ca3acc337219}

此示例代码请求在指定公司中使用的资产名称。 响应会返回一组正在使用的资产名称。

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

