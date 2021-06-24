---
description: 生成新密码。
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 18%

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
| `*`密码`*` | `xsd:string` | 是 | 新密码。 |

## 示例 {#section-f580fefdccec46fe95359e3aef0ed17f}

此代码示例会生成密码。 这种情况很不寻常，因为请求只是一个没有任何封闭元素或值的参数。 IPS返回强密码。

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
