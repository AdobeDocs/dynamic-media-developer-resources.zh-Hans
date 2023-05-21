---
description: 設定ICC設定檔中繼資料欄位。
solution: Experience Manager
title: batchSetIccProfileField
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 14%

---

# batchSetIccProfileField{#batchseticcprofilefields}

設定ICC設定檔中繼資料欄位。

语法

## 授權的使用者型別 {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**輸入(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理包含ICC設定檔的公司。 |
| 更新陣列 | `xsd:string` | 是 | ICC設定檔更新的陣列。 |

**輸出(batchSetIccProfileFields)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 成功設定的ICC設定檔欄位數目。 |
| warningCount | `xsd:int` | 是 | 作業嘗試設定ICC設定檔欄位時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試設定ICC設定檔欄位時產生的錯誤數目。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生警告。 |
| errorDetailArray | `types:AssetOperationFaultArray` | 否 | 與資產關聯的詳細資訊陣列，在作業嘗試套用更新時產生錯誤。 |

## 示例 {#section-5dc90cfbd9b1411485b44859032f7cb9}

**请求**

```java {.line-numbers}
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**响应**

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
