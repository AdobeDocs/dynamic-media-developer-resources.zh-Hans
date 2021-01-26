---
description: 获取指定列表的活动发布上下文的公司。 如果为上下文定义了至少一个活动服务器，则将发布上下文视为活动上下文。
seo-description: 获取指定列表的活动发布上下文的公司。 如果为上下文定义了至少一个活动服务器，则将发布上下文视为活动上下文。
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Dynamic Media Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

---


# getActivePublishContext{#getactivepublishcontext}

获取指定列表的活动发布上下文的公司。 如果为上下文定义了至少一个活动服务器，则将发布上下文视为活动上下文。

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
| `*`companyHandle`*` | `xsd:string` | 是 | 活动发布公司的查询的句柄 |

**输出(getActivePublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | 是 | 活动发布上下文的数组，其中可能包含来自Publish Context的零个或多个值。 |

