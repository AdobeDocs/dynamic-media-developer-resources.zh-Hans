---
description: 重新命名專案。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 23%

---

# renameProject{#renameproject}

重新命名專案。

语法

## 授權的使用者型別 {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-43ccd77648784be4a259a723c3e1db40}

**輸入(renameProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyName | `xsd:string` | 是 | 處理具有您要重新命名專案的公司。 |
| projectHandle | `xsd:string` | 是 | 處理專案。 |
| projectName | `xsd:string` | 是 | 新專案名稱。 |

**輸出(renameProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| projectHandle | `xsd:string` | 是 | 重新命名專案的控點。 |

## 示例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此程式碼範例會重新命名專案並傳回專案控制代碼。

**请求**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**响应**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```
