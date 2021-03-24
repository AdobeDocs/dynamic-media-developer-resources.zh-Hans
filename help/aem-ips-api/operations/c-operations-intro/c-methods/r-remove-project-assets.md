---
description: 从项目中删除资源。 不会销毁资产。
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 10%

---


# removeProjectAssets{#removeprojectassets}

从项目中删除资源。 不会销毁资产。

语法

## 授权用户类型{#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-169d8e317417415b87df86242f65710e}

**输入(removeProjectAssetsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要移动的资产的公司的句柄。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 要移动的项目资产的句柄。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要移动的资产的句柄数组。 |

**输出(removeProjectAssetsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 已成功删除资产计数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试从项目中删除资产时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试从项目中删除资源时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试将资产从项目中删除时生成警告的与资产关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试从项目中删除时生成错误的与资产关联的详细信息数组。 |

## 示例 {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

此代码示例从项目中删除2个资产（由项目句柄指定）。

**请求**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

