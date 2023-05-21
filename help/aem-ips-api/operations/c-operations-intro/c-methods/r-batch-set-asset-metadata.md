---
description: 使用批次模式設定資產中繼資料。
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 13%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

使用批次模式設定資產中繼資料。

语法

## 授權的使用者型別 {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-7111ac93bc7747f69ba14db4ac3912b0}

**輸入(batchSetAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 要在批次作業中設定其中繼資料之公司的控制代碼。 |
| updatearray | `types:BatchMetadataUpdateArray` | 是 | 套用至資產的中繼資料更新陣列。 |

**輸出(batchSetAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定中繼資料的數目。 |
| warningCount | `xsd:int` | 是 | 作業嘗試設定中繼資料時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定中繼資料時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 當作業嘗試批次設定資產的中繼資料時，與產生警告的資產相關聯的詳細資訊陣列。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試批次設定資產的中繼資料時產生錯誤。 |

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
