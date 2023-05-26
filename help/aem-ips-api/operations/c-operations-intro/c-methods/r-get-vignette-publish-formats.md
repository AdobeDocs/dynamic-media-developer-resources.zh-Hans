---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6e56d68e-b5cf-4044-9c58-f8221fa4490f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 24%

---

# getVignettePublishFormats{#getvignettepublishformats}

语法

## 授权的用户类型 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**输入(getVignettePublishFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的把手。 |

**输出(getVignettePublishFormatsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| vignetteFormatArray | `types:VignettePublishFormatArray` | 是 | 晕影发布格式的数组。 |

## 示例 {#section-2cc32b27cc6243b7b3e273cc05996226}

此代码示例返回与特定公司关联的两种晕影发布格式。 信息在数组中返回，为简短起见，该数组会被截断。

**请求**

```java
<getVignettePublishFormatsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
</getVignettePublishFormatsParam>
```

**响应**

```java
<getVignettePublishFormatsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatArray>
      <items>
         <companyHandle>c|21</companyHandle>
         <vignetteFormatHandle>v|21|281</vignetteFormatHandle>
         <name>APIcreateVignettePublishFormat</name>
         ...
      </items>
   </vignetteFormatArray>
</getVignettePublishFormatsReturn>
```
