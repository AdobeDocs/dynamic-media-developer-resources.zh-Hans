---
description: 设置一个或多个资源的缩略图图像。
solution: Experience Manager
title: Batchsetthumbasset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 11%

---

# Batchsetthumbasset{#batchsetthumbasset}

设置一个或多个资源的缩略图图像。

语法

## 缩略图资源类型 {#section-4edc2a6a8f824213b0aaddb1d437268c}

允许的缩略图资源类型包含以下内容：

* 图像
* AdjustedView
* 蒙版
* 模板
* Psd模板

## 授权用户类型 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有目标资产的读/写访问权限，以及缩略图资产的读访问权限。

## 参数 {#section-9c6efa000b384b3db6c013def20cf40b}

**输入(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含资产的公司的句柄。 |
| updateArray | `types:ThumbAssetUpdateArray` | 是 | 更新的数组。 |

**输出(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功设置的缩略图数。 |
| warningcount | `xsd:int` | 是 | 操作尝试设置缩略图时生成的警告数。 |
| errorCount | `xsd:int` | 是 | 操作尝试设置缩略图时生成的错误数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，在操作尝试应用更新时这些资产会生成警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 与资产关联的详细信息数组，当操作尝试应用更新时这些资产会生成错误。 |

## 示例 {#section-6de69a8680c24c1486c5f01488393381}

**请求**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**响应**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
