---
description: 描述用户所属的不同公司。
seo-description: 描述用户所属的不同公司。
seo-title: 公司会员
solution: Experience Manager
title: 公司会员
topic: Dynamic Media Image Production System API
uuid: fc0ddcdd-ad1e-487c-8ef1-9c09e5dca33d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 14%

---


# CompanyMember{#companymember}

描述用户所属的不同公司。

语法

## 参数 {#section-03238fa4af3547f89faa1db91ccfd191}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`用户`*` | `types:User` | 使用者名稱. |
| `*`角色`*` | `xsd:string` | 用户对其所属的每个公司具有的角色。 |
| `*`isActive`*` | `xsd:boolean` | 为用户所属的每个公司设置用户的状态。 |

