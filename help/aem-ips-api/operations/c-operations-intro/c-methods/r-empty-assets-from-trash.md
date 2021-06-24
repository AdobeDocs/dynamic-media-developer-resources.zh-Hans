---
description: 清空IPS垃圾桶中的资产。
solution: Experience Manager
title: emptyAssetsFromTrashe
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 7%

---

# emptyAssetsFromTrashe{#emptyassetsfromtrash}

清空IPS垃圾桶中的资产。

资产会一直存放在垃圾桶中，直到被手动清空，或者超时从垃圾桶中清空。 如果手动清空这些清空文件，则它们会一直存在在垃圾桶中，直到最终从系统中清除它们时（通常是夜间清除）下一个清理作业为止。 如果资产超时进入垃圾桶，则会作为同一清理活动的一部分清理资产。 超时可进行配置（默认为7天）。

## 授权用户类型 {#section-24dee2bf5f9f4714a64955c80f2803b4}

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

**输出(emptyAssetsFromTrasheParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | 是 | 成功从垃圾桶清空的资产数。 |
| `*`warningCount`*` | `xsd:Int` | 是 | 操作尝试从垃圾桶中清空资产时生成的警告数。 |
| `*`errorCount`*` | `xsd:Int` | 是 | 操作尝试从垃圾桶中清空资产时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试从垃圾桶中清空资产时，资产会生成警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试从垃圾桶中清空资产时，资产会生成错误。 |

## 示例 {#section-6154a873b6c342bf92e2036280cafdcf}

此代码示例使用公司的句柄和一个资产句柄数组，其中包含要从垃圾桶中清空的资产的句柄。

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
