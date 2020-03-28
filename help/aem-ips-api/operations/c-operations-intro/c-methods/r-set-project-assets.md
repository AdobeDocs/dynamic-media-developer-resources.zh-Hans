---
description: 在项目中分配或更新资产。
seo-description: 在项目中分配或更新资产。
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setProjectAssets{#setprojectassets}

在项目中分配或更新资产。

语法

## 授权用户类型 {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**输入(setProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | 是 | 公司手柄。 |
| ` *`projectHandle`*` | `xsd:string` | 是 | 项目句柄。 |
| ` *`assetHandleArray`*` | `types:HandleArray` | 是 | 要与项目关联的资产句柄数组。 |

**输出(setProjectAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | 是 | 已成功添加的资产数。 |

## 示例 {#section-33c1a909c3dc4aa98da474c23a036596}

此代码示例将资产分配给项目。 该请求将返回一个成功计数。

**请求**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**响应**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

