---
description: 获取有关用户的信息。 使用系统用户的电子邮件地址和密码作为对请求授权的凭据。 否则，操作将获取有关默认用户的信息。
seo-description: 获取有关用户的信息。 使用系统用户的电子邮件地址和密码作为对请求授权的凭据。 否则，操作将获取有关默认用户的信息。
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 9%

---


# getUserInfo{#getuserinfo}

获取有关用户的信息。 使用系统用户的电子邮件地址和密码作为对请求授权的凭据。 否则，操作将获取有关默认用户的信息。

语法

## 授权用户类型{#section-1c42d78e914a4b84a946b3480f29b36a}

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
| `*`userInfo`*` | `types:User` | 是 | 用户的名字、姓氏、电子邮件地址和角色，以及用户是否有效以及用户密码何时过期。 |

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

