---
description: 使用批处理模式设置资源元数据。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

使用批处理模式设置资源元数据。

语法

## 授权用户类型 {#section-5310d9fd00604cbf9756944900378855}

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
| companyHandle | `xsd:string` | 是 | 要在批处理操作中设置其元数据的公司的句柄。 |
| updateArray | `types:BatchMetadataUpdateArray` | 是 | 应用于资源的元数据更新数组。 |

**输出(batchSetAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功设置元数据的数量。 |
| warningcount | `xsd:int` | 是 | 操作尝试设置元数据时生成的警告数。 |
| errorCount | `xsd:int` | 是 | 操作尝试设置元数据时生成的错误数。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 与资源关联的详细信息数组，当操作尝试批量设置资源的元数据时会生成警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 与资源关联的详细信息数组，当操作尝试批量设置资源的元数据时会生成错误。 |

## 示例 {#section-2de798ac920e4b47b971b1729a64395b}

**请求**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
