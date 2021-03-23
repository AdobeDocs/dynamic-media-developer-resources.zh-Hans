---
description: 返回图像格式，如PDF、EPS、SWF等。
seo-description: 返回图像格式，如PDF、EPS、SWF等。
seo-title: getImageFormats
solution: Experience Manager
title: getImageFormats
uuid: 0adf989d-9c72-4337-99c0-de6931943e78
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 16%

---


# getImageFormats{#getimageformats}

返回图像格式，如PDF、EPS、SWF等。

语法

## 授权用户类型{#section-6a386ad8641b4aa1a281600fc94fd3f6}

* `IpsUser`
* `IspAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-eefa36a70b74498f8727ef61d98cfb63}

**Input(getImageFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 使用要获取的图像格式的公司的句柄。 |

**输出(getImageFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`imageFormatArray`*` | `types:ImageFormatArray` | 是 | 图像格式数组。 |

## 示例 {#section-73881e12839b4904bf3299b0920bdd0c}

此代码示例返回指定公司的所有图像格式。

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

