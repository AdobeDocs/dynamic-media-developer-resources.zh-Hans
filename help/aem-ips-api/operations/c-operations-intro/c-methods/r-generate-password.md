---
description: 生成新密码。
seo-description: 生成新密码。
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 16%

---


# generatePassword{#generatepassword}

生成新密码。

语法

## 授权用户类型{#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-d516615c906240819a284786efb19863}

**Input(generatePasswordParam)**

无。

**输出(generatePasswordParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`密码`*` | `xsd:string` | 是 | 新密码。 |

## 示例 {#section-f580fefdccec46fe95359e3aef0ed17f}

此代码示例生成密码。 这是不寻常的，因为请求只是一个没有任何封闭元素或值的参数。 IPS返回强口令。

**请求**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**响应**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```

