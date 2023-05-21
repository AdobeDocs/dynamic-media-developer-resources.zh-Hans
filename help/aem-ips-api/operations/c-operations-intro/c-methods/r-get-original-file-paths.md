---
description: 取得公司資產的原始檔案路徑。
solution: Experience Manager
title: getOriginalFilePath
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 16%

---

# getOriginalFilePath{#getoriginalfilepaths}

取得公司資產的原始檔案路徑。

语法

## 授權的使用者型別 {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>需要資產的讀取存取權。

## 参数 {#section-a6b394daba6e49a8882cf3051035d9d1}

**輸入(getOriginalFilePathsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |
| assetHandleArray | `types:HandleArray` | 是 | 要取得其原始檔案路徑的資產的控制點陣列。 |

**輸出(getOriginalFilePathsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 原始檔案陣列 | `types:StringArray` | 是 | 代表原始檔案路徑的字串陣列。 |

## 示例 {#section-a966e783a2ba49f5b6b0f961329ab2f8}

此程式碼範例會傳回資產控制代碼陣列中，以唯一資產控制代碼指定的資產檔案路徑。

**请求**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**响应**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```
