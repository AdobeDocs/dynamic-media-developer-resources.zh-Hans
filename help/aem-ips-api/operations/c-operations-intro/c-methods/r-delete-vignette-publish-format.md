---
description: 删除晕影发布格式。
seo-description: 删除晕影发布格式。
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
topic: Dynamic Media Image Production System API
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 13%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

删除晕影发布格式。

## 授权用户类型{#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-789625ba29df4b5f880914d4c64f77ce}

**输入(deleteVignettePublishFormatParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 暗角所属公司的手柄。 |
| `*`vignetteFormatHandle`*` | `xsd:string` | 是 | 要删除的晕影发布格式的句柄。 |

**输出(deleteVignettePublishFormatParam)**

IPS API不返回此操作的响应。

## 示例 {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

此代码范例将删除由其句柄指定的暗角发布格式。

**请求**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**响应**

无。
