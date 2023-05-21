---
description: 取得使用者的相關資訊。 使用系統使用者的電子郵件地址和密碼作為授權請求的認證。 否則，操作會取得預設使用者的相關資訊。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# getUserInfo{#getuserinfo}

取得使用者的相關資訊。 使用系統使用者的電子郵件地址和密碼作為授權請求的認證。 否則，操作會取得預設使用者的相關資訊。

语法

## 授權的使用者型別 {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-e87b3cb743494719925c9458eed433b6}

**輸入(getUserInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userHandle | `xsd:string` | 否 | 處理您要傳回其資訊的使用者。 |
| 电子邮件 | `xsd:string` | 否 | 使用者電子郵件地址。 |

**輸出(getUserInfoReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| userInfo | `types:User` | 是 | 使用者的名字、姓氏、電子郵件地址和角色，以及使用者是否有效和使用者密碼何時到期。 |

## 示例 {#section-98d77a2e360a438dbe240099bea26a65}

此程式碼範例會傳回預設IPS使用者的資訊。

**请求**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**响应**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
