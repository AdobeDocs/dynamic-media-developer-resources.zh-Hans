---
description: 在项目中分配或更新资产。
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 18%

---


# setProjectAssets{#setprojectassets}

在项目中分配或更新资产。

语法

## 授权用户类型{#section-8d87939db6d547b48ca6d71771bbefa8}

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
| `*`companyName`*` | `xsd:string` | 是 | 公司手柄。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 项目句柄。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要与项目关联的资产句柄的数组。 |

**输出(setProjectAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功添加的资产数。 |

## 示例 {#section-33c1a909c3dc4aa98da474c23a036596}

此代码示例将资产分配给项目。 请求返回成功计数1。

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

