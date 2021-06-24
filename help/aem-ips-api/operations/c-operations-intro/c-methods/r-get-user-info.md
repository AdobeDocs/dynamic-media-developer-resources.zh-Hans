---
description: 获取有关用户的信息。 使用系统用户的电子邮件地址和密码作为授权请求的凭据。 否则，操作将获取有关默认用户的信息。
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 11%

---

# getUserInfo{#getuserinfo}

获取有关用户的信息。 使用系统用户的电子邮件地址和密码作为授权请求的凭据。 否则，操作将获取有关默认用户的信息。

语法

## 授权用户类型 {#section-1c42d78e914a4b84a946b3480f29b36a}

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

**输入(getUserInfoParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | 否 | 处理要返回其信息的用户。 |
| `*`电子邮件`*` | `xsd:string` | 否 | 用户电子邮件地址。 |

**输出(getUserInfoReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | 是 | 用户的名字、姓氏、电子邮件地址和角色，以及用户是否有效以及用户密码过期的时间。 |

## 示例 {#section-98d77a2e360a438dbe240099bea26a65}

此代码示例返回默认IPS用户的信息。

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
