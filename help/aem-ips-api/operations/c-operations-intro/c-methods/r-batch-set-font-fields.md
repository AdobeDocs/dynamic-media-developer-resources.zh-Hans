---
description: 設定字型中繼資料欄位。
solution: Experience Manager
title: batchsetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 15%

---

# batchsetFontFields{#batchsetfontfields}

設定字型中繼資料欄位。

## 授權的使用者型別 {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-836f5948d00a46e98ccb62f0573e4e68}

**輸入(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理包含字型的公司。 |
| updatearray | `types:FontFieldUpdateArray` | 是 | 字型欄位更新的陣列。 |

**輸出(batchSetFontFieldsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定的字型欄位數目。 |
| warningCount | `xsd:int` | 是 | 作業嘗試設定字型欄位時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定字型欄位時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生錯誤。 |

## 示例 {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**请求**

```javascript {.line-numbers}
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**响应**

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```
