---
description: 删除晕影发布格式。
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic，SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 13%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

删除晕影发布格式。

## 授权用户类型 {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-789625ba29df4b5f880914d4c64f77ce}

**输入(deleteVignettePublishFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 晕影所属公司的把手。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 要删除的晕影发布格式的句柄。 |

**输出(deleteVignettePublishFormatParam)**

IPS API不会返回此操作的响应。

## 示例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

此代码示例会删除由其句柄指定的晕影发布格式。

**请求**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**响应**

无。
