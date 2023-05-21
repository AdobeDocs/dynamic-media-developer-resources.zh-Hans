---
description: 設定資產的中繼資料值。 使用一系列中繼資料更新，以設定批次中的值。
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 10%

---

# setAssetMetadata{#setassetmetadata}

設定資產的中繼資料值。 使用一系列中繼資料更新，以設定批次中的值。

语法

## 授權的使用者型別 {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有資產的讀取存取權。

## 参数 {#section-bcdcff30905e444388811e897b2824bd}

**輸入(setAssetMetadataParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有您要更新之資產的公司的控制代碼。 |
| assetHandle | `xsd:string` | 是 | 資產的控點。 |
| updatearray | `types:MetadataUpdateArray` | 是 | 中繼資料更新陣列中的更新。 |

**輸出(setAssetMetadataReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-1ab412e7ee1d4d6d8469b0b403598c42}

此程式碼範例使用一系列中繼資料更新來設定指定資產的中繼資料。

**请求**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**响应**

无。
