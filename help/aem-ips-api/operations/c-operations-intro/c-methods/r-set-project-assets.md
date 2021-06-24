---
description: 分配或更新项目中的资产。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

分配或更新项目中的资产。

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
| `*`companyName`*` | `xsd:string` | 是 | 公司负责人。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 项目句柄。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要与项目关联的资产句柄数组。 |

**输出(setProjectAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功添加的资产数。 |

## 示例 {#section-33c1a909c3dc4aa98da474c23a036596}

此代码示例可将资产分配到项目。 该请求会返回一个成功计数。

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
