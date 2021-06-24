---
description: 重命名项目。
solution: Experience Manager
title: renameProject
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: 1bf74ebf-1fce-408b-9953-7fdf2ae9d10b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 21%

---

# renameProject{#renameproject}

重命名项目。

语法

## 授权用户类型 {#section-093d1f611a1647568e885ddd842b8f78}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-43ccd77648784be4a259a723c3e1db40}

**输入(renameProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | 是 | 处理包含要重命名项目的公司。 |
| `*`projectHandle`*` | `xsd:string` | 是 | 处理项目。 |
| `*`projectName`*` | `xsd:string` | 是 | 新项目名称。 |

**输出(renameProjectParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | 是 | 重命名项目的句柄。 |

## 示例 {#section-a0a06d9244774795b695a10b92b2a5e7}

此代码示例将重命名项目并返回项目句柄。

**请求**

```java
<renameProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ApiTestProject</projectHandle>
   <projectName>ProjectTestAPI</projectName>
</renameProjectParam>
```

**响应**

```java
<renameProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
</renameProjectReturn>
```
