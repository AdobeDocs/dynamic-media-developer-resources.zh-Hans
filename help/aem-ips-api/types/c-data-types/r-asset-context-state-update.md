---
description: 为与资产关联的发布上下文设置一组新的发布状态标记。
solution: Experience Manager
title: AssetContextStateUpdate
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---

# AssetContextStateUpdate{#assetcontextstateupdate}

为与资产关联的发布上下文设置一组新的发布状态标记。

**参数**

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 处理要更新的资产。 |
| `*`contextStateUpdateArray`*` | `types:ContextStateUpdateArray` | 要更新的资产的发布联系状态数组。 |
