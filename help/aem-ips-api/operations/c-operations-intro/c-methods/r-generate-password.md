---
description: 生成新密码。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 20%

---

# generatePassword{#generatepassword}

生成新密码。

语法

## 授权用户类型 {#section-88f7dc11e5c74be281399d8f2e3c9555}

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

**输入(generatePasswordParam)**

无。

**输出(generatePasswordParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 密码 | `xsd:string` | 是 | 新密码。 |

## 示例 {#section-f580fefdccec46fe95359e3aef0ed17f}

此代码示例生成一个密码。 此请求不常见，因为请求只是一个参数，没有任何包含的元素或值。 IPS返回强密码。

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
