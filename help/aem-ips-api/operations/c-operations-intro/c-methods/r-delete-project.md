---
description: 从公司中删除项目。 资源与项目之间的链接将断开，但不会从IPS中删除资源。
seo-description: 从公司中删除项目。 资源与项目之间的链接将断开，但不会从IPS中删除资源。
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 7%

---


# deleteProject{#deleteproject}

从公司中删除项目。 资源与项目之间的链接将断开，但不会从IPS中删除资源。

语法

## 授权用户类型{#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-00d1e00dd5014513a52b4e6b4f61de62}

**输入(deleteProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 与项目关联的公司的名称。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 要删除的项目的句柄。 |

**输出(deleteProjectReturn)**

IPS API不返回此操作的响应。

## 示例 {#section-e38507f1f7ec41b9a625f47390490254}

此代码示例使用公司句柄和项目句柄作为发送到IPS Web服务器的deleteProjectParam中的字段来删除项目。

**请求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**响应**

无。
