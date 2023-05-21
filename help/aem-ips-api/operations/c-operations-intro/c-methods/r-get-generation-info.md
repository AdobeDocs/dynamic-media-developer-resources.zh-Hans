---
description: 根據傳入的引數，傳回2種不同型別的資訊。 originatorHandle會傳回從指定資產產生之資產的相關資訊。 generateHandle會傳回用來產生指定資產或檔案之步驟的相關資訊。
solution: Experience Manager
title: getGenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fa098e3c-8145-4238-a84c-c545f1c53341
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 10%

---

# getGenerationInfo{#getgenerationinfo}

根據傳入的引數，傳回2種不同型別的資訊。 originatorHandle會傳回從指定資產產生之資產的相關資訊。 generateHandle會傳回用來產生指定資產或檔案之步驟的相關資訊。

语法

## 授權的使用者型別 {#section-9cc2216b32c74107be07aeacecc11401}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-b7fa94c82147455888e8469fa5f6922b}

**輸入(getGenerationInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 程式碼片語 | `xsd:string` | 是 | 公司的控制代碼。 |
| 程式碼片語 | `xsd:string` | 否 | 產生時使用的引擎。 請參閱字型樣式。 |
| 程式碼片語 | `xsd:string` | 否 | 要查詢所產生資產的資產控制代碼。 |
| 程式碼片語 | `xsd:string` | 否 | 要查詢其產生中使用的資產和引擎的資產控制代碼。 |
| 程式碼片語 | `xsd:StringArray` | 否 | 作業中包含的屬性。 |
| 程式碼片語 | `xsd:StringArray` | 否 | 從作業排除的屬性。 |

**輸出(getGenerationInfoReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| generationArray | `types:GenerationInfoArray` | 是 | 層代資訊的陣列。 |

## 示例 {#section-fdffe6ed82d94c7aa90e47f7ce889403}

此程式碼範例會傳回有關從特定資產產生之資產的資訊。 它不會擷取有關用於產生指定資產的步驟的資訊。 為簡短起見，回應會遭截斷。

**请求**

```java
<getGenerationInfoParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <originatorHandle>a|716|25|160</originatorHandle>
</getGenerationInfoParam>
```

**响应**

```java
<getGenerationInfoReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <generationArray>
      <items>
         <engine>PostScriptRip</engine>
         <originator>
         ...
         </generated>
         <attributeArray/>
      </items>
   </generationArray>
</getGenerationInfoReturn>
```
