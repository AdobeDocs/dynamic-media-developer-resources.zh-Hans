---
description: 建立新專案。
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 19%

---

# createProject{#createproject}

建立新專案。

语法

## 授權的使用者型別 {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-8c741884eb54489bbaad0c444fee80b6}

**輸入(createProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 與新專案相關聯之公司的控制代碼。 |
| projectName | `xsd:string` | 是 | 新專案名稱。 |

**輸出(createProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| projectHandle | `xsd:string` | 是 | 新專案的控點。 |

## 示例 {#section-a0cd532b67e346d088fbec141231a0e5}

此程式碼範例會建立名為的專案 `ApiTestProject` 在由其控制代碼指定的公司中。 回應會將控制代碼傳回至專案。

**请求**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```
