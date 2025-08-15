---
title: emptyAssetsFromTrash
description: 清空IPS垃圾桶中的资源。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 6%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

清空IPS垃圾桶中的资源。

Assets一直存放在垃圾桶中，直到手动清空它们或将它们从垃圾桶中取出。 如果手动清空，则它们会留在垃圾桶中，直到下次清理作业（通常在夜间）最终从系统中清除时为止。 如果资源在垃圾桶中超时，则在同一清理活动中会清理这些资源。 超时可配置（默认值为7天）。

## 授权用户类型 {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8e1fb0ee3aae453581e99ef76e298569}

**输入(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | xsd:string | 是 | 拥有资产的公司的句柄。 |
| assetHandleArray | 类型:HandleArray | 是 | 表示要从垃圾桶中清空的项目的句柄数组。 |

**输出(emptyAssetsFromTrashParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | xsd:Int | 是 | 成功从垃圾桶中清空的资源数。 |
| warningcount | xsd:Int | 是 | 操作尝试从垃圾桶中清空资源时生成的警告数。 |
| errorCount | xsd:Int | 是 | 操作尝试从垃圾桶清空资源时生成的错误数。 |
| warningDetailArray | 类型:AssetOperationFaultArray | 否 | 与资源关联的详细信息数组，在操作尝试从垃圾桶清空资源时这些资源会生成警告。 |
| errorDetailArray | 类型:AssetOperationFaultArray | 否 | 与资源关联的详细信息数组，在操作尝试从垃圾桶清空资源时这些资源会生成错误。 |

## 示例 {#section-6154a873b6c342bf92e2036280cafdcf}

此代码示例使用公司的句柄和一个资源句柄数组，该数组包含要从垃圾桶中清空的资源的句柄。

**请求**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**响应**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
