---
description: 從標籤欄位的字典中移除標籤欄位值。
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2694bd6d-b1ba-4146-a155-12829d9dfa47
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 13%

---

# deleteTagFieldValues{#deletetagfieldvalues}

從標籤欄位的字典中移除標籤欄位值。

## 授權的使用者型別 {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## 参数 {#section-5db64a6ae238426395bc760b83587260}

**輸入(deleteTagFieldValuesParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 包含標籤欄位之公司的控制代碼。 |
| fieldHandle | `xsd:string` | 是 | 要修改之標籤欄位的控點。 |
| valueArray | `types:StringArray` | 是 | 要從欄位字典中刪除的標籤值陣列。 |

**輸出(deleteTagFieldValuesParam)**

IPS API未傳回此作業的回應。

## 示例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**请求**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**响应**

无。
