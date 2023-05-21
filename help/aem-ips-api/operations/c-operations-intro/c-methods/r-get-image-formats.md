---
description: 傳回影像格式，例如PDF、EPS、SWF等。
solution: Experience Manager
title: getImageFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c2fa4cdd-fb4f-4e6a-8197-8f64c986c3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 20%

---

# getImageFormats{#getimageformats}

傳回影像格式，例如PDF、EPS、SWF等。

语法

## 授權的使用者型別 {#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-eefa36a70b74498f8727ef61d98cfb63}

**輸入(getImageFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 具有您要取得之影像格式的公司控制代碼。 |

**輸出(getImageFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| imageFormatArray | `types:ImageFormatArray` | 是 | 影像格式陣列。 |

## 示例 {#section-73881e12839b4904bf3299b0920bdd0c}

此程式碼範例會傳回指定公司的所有影像格式。

**请求**

```java
<ns1:getImageFormatsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getImageFormatsParam>
```

**响应**

```java
<getImageFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <imageFormatArray></imageFormatArray>
</getImageFormatsReturn>
```
