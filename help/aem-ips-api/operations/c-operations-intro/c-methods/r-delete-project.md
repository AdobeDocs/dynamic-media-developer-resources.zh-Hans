---
description: 從公司刪除專案。 資產和專案之間的連結已中斷，但資產不會從IPS中刪除。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 9%

---

# deleteProject{#deleteproject}

從公司刪除專案。 資產和專案之間的連結已中斷，但資產不會從IPS中刪除。

语法

## 授權的使用者型別 {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-00d1e00dd5014513a52b4e6b4f61de62}

**輸入(deleteProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyName | `xsd:string` | 是 | 與專案相關聯的公司名稱。 |
| projectHandle | `xsd:string` | 是 | 要刪除的專案的控制代碼。 |

**輸出(deleteProjectReturn)**

IPS API未傳回此作業的回應。

## 示例 {#section-e38507f1f7ec41b9a625f47390490254}

此程式碼範例使用公司控制代碼和專案控制代碼作為傳送到IPS Web服務伺服器的deleteProjectParam中的欄位，以刪除專案。

**请求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**响应**

无。
