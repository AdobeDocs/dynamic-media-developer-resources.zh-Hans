---
description: 获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

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

