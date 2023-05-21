---
description: 刪除影像格式。 從saveImageFormat取得影像格式控制代碼。
solution: Experience Manager
title: deleteImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: bd717c08-6da4-47f1-8614-e4ba79d8176c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 11%

---

# deleteImageFormat{#deleteimageformat}

刪除影像格式。 從saveImageFormat取得影像格式控制代碼。

语法

## 授權的使用者型別 {#section-827e24a3019543418b0a635d46c1edfd}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-462c05d9aad746ee8d2be0656041b693}

**輸入(deleteImageFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含您要刪除之影像格式的公司控制代碼。 |
| imageFormatHandle | `xsd:string` | 是 | 您要刪除之影像格式的控點。 |

**輸出(deleteImageFormatParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-9ed9baaba13549bfaad1bc9cd7ec7009}

此程式碼範例會從公司刪除影像格式。 從其他作業取得影像格式控制代碼。

**请求**

```java
<deleteImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <imageFormatHandle>47|301</imageFormatHandle>
</deleteImageFormatParam>
```

**响应**

无。

**相關主題：**

[saveImageFormat](../../../operations/c-operations-intro/c-methods/r-save-image-format.md#reference-d15c27f533ef41e38b54a539a304bd1d)
