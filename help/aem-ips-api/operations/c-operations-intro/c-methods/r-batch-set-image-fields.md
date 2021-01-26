---
description: 为一个或多个图像资产设置特定于图像的字段。
seo-description: 为一个或多个图像资产设置特定于图像的字段。
seo-title: batchSetImageFields
solution: Experience Manager
title: batchSetImageFields
topic: Dynamic Media Image Production System API
uuid: e0ad7da4-cb28-4402-8b47-a600916d23b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 9%

---


# batchSetImageFields{#batchsetimagefields}

为一个或多个图像资产设置特定于图像的字段。

语法

## 授权用户类型{#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4969815cf67c4d11b13bb2017b3604e8}

**输入(batchSetImageFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含图像资产的公司的句柄。 |
| `*`updateArray`*` | `types:ImageFieldUpdateArray` | 是 | 图像字段更新的数组。 |

**输出(batchSetImageFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功设置图像字段的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试设置图像字段时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试设置图像字段时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试应用更新时生成警告的与资产关联的详细信息数组。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试应用更新时生成错误的与资产关联的详细信息数组。 |

## 示例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

此示例在一个更新数组中设置两个图像的字段中的数据。 在数组中，图像由其资产句柄指定，包含分辨率（以像素为单位）、X和Y位置锚点坐标以及用户数据。 响应表示已成功设置两个图像的字段。

**请求**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**响应**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```

