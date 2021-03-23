---
description: 从废纸篓恢复资源。
seo-description: 从废纸篓恢复资源。
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

从废纸篓恢复资源。

语法

## 授权用户类型{#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-200a61d040c94e489a85241b29cd499a}

**输入(restoreAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 对要恢复的资产的公司的处理。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 要恢复的资产的句柄数组。 |

**输出(restoreAssetsFromTrashReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 从垃圾桶中成功删除的资源数。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试从垃圾桶中恢复资源时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 尝试从废纸篓恢复资源时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试从废纸篓中恢复资源时生成警告的与资源关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与在操作尝试从垃圾桶中恢复资源时生成错误的资源关联的详细信息数组。 |

## 示例 {#section-98fe0394b0634ca397c395f14f8a9358}

此代码示例可从垃圾桶中恢复资源。 响应指示操作已成功完成。

**请求**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**响应**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

