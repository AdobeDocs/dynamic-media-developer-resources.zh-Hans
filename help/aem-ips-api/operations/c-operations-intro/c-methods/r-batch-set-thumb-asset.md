---
description: 設定一或多個資產的縮圖影像。
solution: Experience Manager
title: batchsetthumbasset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 12%

---

# batchsetthumbasset{#batchsetthumbasset}

設定一或多個資產的縮圖影像。

语法

## 縮圖資產型別 {#section-4edc2a6a8f824213b0aaddb1d437268c}

允許的縮圖資產型別包含下列專案：

* 图像
* AdjustedView
* 遮色片
* 模板
* Psd範本

## 授權的使用者型別 {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有目標資產的讀取/寫入存取權，以及縮圖資產的讀取存取權。

## 参数 {#section-9c6efa000b384b3db6c013def20cf40b}

**輸入(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含資產的公司的控制代碼。 |
| updatearray | `types:ThumbAssetUpdateArray` | 是 | 更新的陣列。 |

**輸出(batchSetThumbAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定的縮圖數目。 |
| warningCount | `xsd:int` | 是 | 作業嘗試設定縮圖時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定縮圖時產生的錯誤數目。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生錯誤。 |

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
