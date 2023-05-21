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

## 授權的使用者型別 {#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**輸入(getVignettePublishFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司的控制代碼。 |

**輸出(getVignettePublishFormatsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| vignetteformatArray | `types:VignettePublishFormatArray` | 是 | 暈映發佈格式的陣列。 |

## 示例 {#section-2cc32b27cc6243b7b3e273cc05996226}

此程式碼範例會傳回與特定公司相關聯的兩個暈映發佈格式。 傳回的資訊會以陣列傳回，為簡短起見，該陣列會遭到截斷。

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
