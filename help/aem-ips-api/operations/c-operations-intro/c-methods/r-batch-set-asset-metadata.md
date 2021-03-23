---
description: 使用批处理模式设置资产元数据。
seo-description: 使用批处理模式设置资产元数据。
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
feature: Dynamic Media Classic，SDK/API，Metadata.Asset Management
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 12%

---


# batchSetAssetMetadata{#batchsetassetmetadata}

使用批处理模式设置资产元数据。

语法

## 授权用户类型{#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7111ac93bc7747f69ba14db4ac3912b0}

**输入(batchSetAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要在批处理操作中设置其元数据的公司的句柄。 |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | 是 | 应用于资产的元数据更新的数组。 |

**输出(batchSetAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功设置元数据的数量。 |
| `*`warningCount`*` | `xsd:int` | 是 | 操作尝试设置元数据时生成的警告数。 |
| `*`errorCount`*` | `xsd:int` | 是 | 操作尝试设置元数据时生成的错误数。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试为资产批量设置元数据时，与资产相关联的详细信息数组会生成警告。 |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 在操作尝试为资产批量设置元数据时生成错误的与资产关联的详细信息数组。 |

## 示例 {#section-2de798ac920e4b47b971b1729a64395b}

**请求**

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**响应**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

