---
description: 刪除公司的中繼資料欄位。
solution: Experience Manager
title: deleteMetadataField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1922fc1b-2abc-4d31-985a-65c788af4d46
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deleteMetadataField{#deletemetadatafield}

刪除公司的中繼資料欄位。

语法

## 授權的使用者型別 {#section-63e7d17f4b434995a872838bfff7f9ff}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-73f12a30cc4340b6b32dd11effd5195e}

**輸入(deleteMetadataFieldParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含要刪除之中繼資料欄位之公司的控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 要刪除的中繼資料欄位的控制代碼。 |

**輸出(deleteMetadataFieldParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-e1c474ea91a040609ecd7c2400f4fa3c}

此程式碼範例會刪除公司的中繼資料欄位。 它使用公司控制代碼和中繼資料控制代碼作為中的欄位 `deleteMetadataFieldParam` 傳遞至IPS Web服務伺服器以執行此動作。

**请求**

```java
<deleteMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
</deleteMetadataFieldParam>
```

**响应**

無。0
