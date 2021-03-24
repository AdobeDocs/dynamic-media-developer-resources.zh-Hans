---
description: 设置一个或多个资产的缩略图。
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 13%

---


# batchSetThumbAsset{#batchsetthumbasset}

设置一个或多个资产的缩略图。

语法

## 缩略图资产类型{#section-4edc2a6a8f824213b0aaddb1d437268c}

允许的缩略图资产类型包括：

* 图像
* 调整后的视图
* 蒙版
* 模板
* PsdTemplate

## 授权用户类型{#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用户必须具有对目标资源的读/写访问权限，并具有对缩略图资源的读访问权限。

## 参数 {#section-9c6efa000b384b3db6c013def20cf40b}

**Input(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含资产的公司的句柄。 |
| `*`updateArray`*` | `types:ThumbAssetUpdateArray` | 是 | 更新的数组。 |

**输出(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功设置缩略图的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试设置缩略图时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试设置缩略图时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试应用更新时生成警告的与资产关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 与在操作尝试应用更新时生成错误的资产关联的详细信息数组。 |

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

