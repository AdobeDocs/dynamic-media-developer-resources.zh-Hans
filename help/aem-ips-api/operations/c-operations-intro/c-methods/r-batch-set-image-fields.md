---
description: 設定一或多個影像資產的影像特定欄位。
solution: Experience Manager
title: batchsetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# batchsetImageFields{#batchsetimagefields}

設定一或多個影像資產的影像特定欄位。

语法

## 授權的使用者型別 {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-4969815cf67c4d11b13bb2017b3604e8}

**輸入(batchSetImageFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含影像資產的公司的控制代碼。 |
| updatearray | `types:ImageFieldUpdateArray` | 是 | 影像欄位陣列會更新。 |

**輸出(batchSetImageFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定的影像欄位數。 |
| warningCount | `xsd:int` | 是 | 作業嘗試設定影像欄位時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定影像欄位時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生錯誤。 |

## 示例 {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

此範例會在更新陣列中設定兩個影像欄位中的資料。 在陣列中，影像由其資產控點指定，並包含解析度（以畫素為單位）、x和y位置錨點座標，以及使用者資料。 此回應表示兩個影像的欄位皆已成功設定。

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
