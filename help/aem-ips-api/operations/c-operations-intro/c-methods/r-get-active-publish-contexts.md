---
description: 获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

获取指定公司的活动发布上下文列表。 如果为上下文定义了至少一个活动服务器，则发布上下文被视为活动。

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
| companyHandle | `xsd:string` | 是 | 要查询活动发布上下文的公司句柄 |

**Output(getActivePublishContextsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| contextArray | `types:StringArray` | 是 | 活动发布上下文的数组，其中可能包含来自发布上下文的零个或多个值。 |
