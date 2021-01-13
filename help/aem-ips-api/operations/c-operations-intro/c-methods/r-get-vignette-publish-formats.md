---
description: getVignettePublishFormats
solution: Experience Manager
title: getVignettePublishFormats
topic: Scene7 Image Production System API
uuid: 2cf58002-5c4a-4391-85d4-4a67cb085afa
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 24%

---


# getVignettePublishFormats{#getvignettepublishformats}

语法

## 已授权的用户类型{#section-1f5e2f74aef8408e89ed9ccac8b5b9bc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-ba28150e6d8c4aa0b4ec72451ba7bc71}

**输入(getVignettePublishFormatsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | 是 | 公司的把手。 |

**输出(getVignettePublishFormatsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`vignetteFormatArray`*` | `types:VignettePublishFormatArray` | 是 | 暗角发布格式的数组。 |

## 示例 {#section-2cc32b27cc6243b7b3e273cc05996226}

此代码示例返回与特定公司关联的两种暗角发布格式。 信息在数组中返回，该数组会被截断以简化。

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

