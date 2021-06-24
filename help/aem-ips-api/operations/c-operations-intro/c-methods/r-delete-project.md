---
description: 从公司中删除项目。 资产和项目之间的链接已损坏，但不会从IPS中删除资产。
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 9%

---

# deleteProject{#deleteproject}

从公司中删除项目。 资产和项目之间的链接已损坏，但不会从IPS中删除资产。

语法

## 授权用户类型 {#section-d8a70e23c68d426e9af1357b978ae2f0}

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
| `*`companyName`*` | `xsd:string` | 是 | 与项目关联的公司名称。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 要删除的项目的句柄。 |

**输出(deleteProjectReturn)**

IPS API不会返回此操作的响应。

## 示例 {#section-e38507f1f7ec41b9a625f47390490254}

此代码示例使用公司句柄和项目句柄作为deleteProjectParam中的字段，这些字段发送到IPS Web服务服务器以删除项目。

**请求**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**响应**

无。
