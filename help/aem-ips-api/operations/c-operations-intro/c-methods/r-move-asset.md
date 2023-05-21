---
description: 將資產移至特定資料夾。
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 17%

---

# moveAsset{#moveasset}

將資產移至特定資料夾。

语法

## 授權的使用者型別 {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-dd0bbdf293aa4563af70a91f97c861f1}

**輸入(moveAssetParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetHandle | `xsd:string` | 是 | 處理您要移動的資產。 |
| folderHandle | `xsd:string` | 是 | 目的地資料夾的處理常式。 |

**輸出(moveAssetReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-78333769f4f14e2886fdf06433c9d2ad}

此程式碼範例將資產移至資料夾。

**请求**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**响应**

无。
