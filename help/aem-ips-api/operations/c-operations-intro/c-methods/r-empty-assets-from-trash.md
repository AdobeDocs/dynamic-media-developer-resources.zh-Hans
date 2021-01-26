---
description: 清空IPS垃圾桶中的资源。
seo-description: 清空IPS垃圾桶中的资源。
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Dynamic Media Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

清空IPS垃圾桶中的资源。

资产会一直存放在垃圾桶中，直到被手动清空，或者超出垃圾桶。 如果手动清空它们，它们将一直存放在垃圾桶中，直到最终从系统中清空它们的下一个清除作业（通常是晚上清除）。 如果资产超时从垃圾桶中清除，则会作为同一清理活动的一部分清理资产。 超时是可配置的（默认值为7天）。

## 授权用户类型{#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## 参数 {#section-8e1fb0ee3aae453581e99ef76e298569}

**输入(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 拥有资产的公司的句柄。 |
| `*`assetHandleArray`*` | `types:HandleArray` | 是 | 表示要从垃圾桶中清空的项目的句柄数组。 |

**输出(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | 是 | 从垃圾桶中成功清空的资源数。 |
| `*`warningCount`*` | `xsd:Int` | 是 | 操作尝试从垃圾桶中清空资产时生成的警告数。 |
| `*`errorCount`*` | `xsd:Int` | 是 | 操作尝试从废纸篓清空资产时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试从垃圾桶中清空资产时，这些资产生成了警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试从垃圾桶中清空资产时，这些资产生成了错误。 |

## 示例 {#section-6154a873b6c342bf92e2036280cafdcf}

此代码示例使用公司的句柄和一个资产句柄数组，该数组包含要从垃圾桶中清空的资产的句柄。

**请求**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**响应**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

