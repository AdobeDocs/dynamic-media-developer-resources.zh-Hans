---
description: 取得搜尋字串、關鍵字和資產的其他相關資訊。 回應包含有關資產的其他資訊。
solution: Experience Manager
title: getSearchStrings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e94215b8-1121-4be6-a8a9-e9444c57495d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 17%

---

# getSearchStrings{#getsearchstrings}

取得搜尋字串、關鍵字和資產的其他相關資訊。 回應包含有關資產的其他資訊。

语法

## 授權的使用者型別 {#section-b09c817a59f949a28e1c029e431f5698}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-c1efda4bb15349a68b276bafee8c18fd}

**輸入(getSearchStringsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetHandle | `xsd:string` | 是 | 處理資產。 |

**輸出(getSearchStringsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| searchStringArray | `types:SearchStrings` | 是 | 資產搜尋字串的陣列。 |

## 示例 {#section-e1f73bff6e4440c489d59cb9aa5384d8}

此程式碼範例會傳回資產特定的搜尋字串。 回應會傳回空白陣列。

**请求**

```java
<getSearchStringsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>47</ns1:companyHandle>
   <assetHandle>a|717|1|530</assetHandle>
</getSearchStringsParam>
```

**响应**

无。
