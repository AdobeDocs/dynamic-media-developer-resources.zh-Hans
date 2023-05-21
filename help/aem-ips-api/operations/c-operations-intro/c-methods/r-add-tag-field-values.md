---
description: 將新標籤值新增至現有標籤欄位的字典。
solution: Experience Manager
title: addTagFieldValue
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---

# addTagFieldValue{#addtagfieldvalues}

將新標籤值新增至現有標籤欄位的字典。

语法

## 授權的使用者型別 {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**輸入(addTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 要修改之標籤欄位的控點。 |
| valueArray | `xsd:string` | 是 | 要新增至欄位現有字典的標籤值陣列。 |

**輸出(addTagFieldValuesParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-c4049392f1c548f883b8b1f8f167bada}

**请求**

```java {.line-numbers}
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**响应**

无。
