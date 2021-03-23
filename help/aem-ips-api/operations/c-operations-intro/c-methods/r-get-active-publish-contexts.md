---
description: 获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。
seo-description: 获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---


# getActivePublishContext{#getactivepublishcontext}

获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。

语法

## 授权用户类型{#section-eb22397744434dfe92a59ffa2883c2e7}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 活动发布上下文的公司到查询的句柄 |

**输出(getActivePublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | 是 | 活动发布上下文的数组，其中可能包括Publish Context中的零个或多个值。 |

