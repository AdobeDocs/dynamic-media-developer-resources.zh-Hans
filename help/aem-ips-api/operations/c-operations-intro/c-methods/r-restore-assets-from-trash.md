---
description: 从垃圾桶中恢复资源。
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 11%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

从垃圾桶中恢复资源。

语法

## 授权用户类型 {#section-15e887782c7d4ace897ff02c6ad5baa0}

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
| companyHandle | `xsd:string` | 是 | 包含要恢复的资产的公司的句柄。 |
| assetHandleArray | `types:HandleArray` | 是 | 要还原的资源的句柄数组。 |

**输出(restoreAssetsFromTrashReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功从垃圾桶中删除的资源数。 |
| warningcount | `xsd:int` | 是 | 操作尝试从垃圾桶中还原资源时生成的警告数。 |
| errorCount | `xsd:int` | 是 | 尝试从垃圾桶中还原资源时生成的错误数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 与资源关联的一系列详细信息，这些资源在操作尝试从垃圾桶中还原资源时生成警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 与资源关联的一系列详细信息，这些资源在操作尝试从垃圾桶中还原资源时生成错误。 |

## 示例 {#section-98fe0394b0634ca397c395f14f8a9358}

此代码示例从垃圾桶中还原资源。 响应指示操作已成功完成。

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
