---
description: 获取指定公司的活动发布上下文列表。 如果为发布上下文至少定义了一个活动服务器，则该上下文被视为活动。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

获取指定公司的活动发布上下文列表。 如果为发布上下文至少定义了一个活动服务器，则该上下文被视为活动。

语法

## 授权用户类型 {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 参数 {#section-a4be4024e55c472fa6728faec9c5e048}

**输入(getActivePublishContextsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 公司查询活动发布上下文的句柄 |

**输出(getActivePublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| contextArray | `types:StringArray` | 是 | 活动发布上下文的数组，其中可能包括发布上下文中的零个或多个值。 |

