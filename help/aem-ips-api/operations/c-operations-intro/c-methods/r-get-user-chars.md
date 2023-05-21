---
description: 取得特定欄位中使用的字元清單。
solution: Experience Manager
title: getUserChars
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 12%

---

# getUserChars{#getuserchars}

取得特定欄位中使用的字元清單。

语法

## 授權的使用者型別 {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-93107d87f1b24fc8ad276dfee5e30b63}

**輸入(getUserCharsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| charField | `xsd:string` | 是 | 決定要搜尋的垃圾桶狀態。 |
| includeInactive | `xsd:boolean` | 是 | 包含或排除非作用中的使用者。 非IPS管理員使用者必須是至少一個公司的作用中成員，才能獲得授權進行任何API呼叫。 如果使用者沒有有效的公司成員資格，則會傳回授權錯誤。 |
| includInvalid | `xsd:boolean` | 否 | 包含或排除無效的使用者。 |
| companyHandleArray | `types:HandleArray` | 否 | 根據公司篩選結果。 |
| groupHandleArray | `types:HandleArray` | 否 | 根據群組篩選結果。 |
| userRoleArray | `types:StringArray` | 否 | 根據使用者角色篩選結果。 |
| numChars | `xsd:int` | 否 | 啟用>1個字元。 |

**輸出(getUserCharsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userCharsArray | `types:StringArray` | 是 | 字元首碼的陣列。 |

## 示例 {#section-3702f165e8b041139a6144f4a76ca25f}

此程式碼範例會傳回：

* 特定公司使用者姓氏的第一個字元。
* 一組群組。
* 一組使用者角色。

「使用者字元篩選欄位」字串常數決定傳回的使用者字元型別。

**请求**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**响应**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```
