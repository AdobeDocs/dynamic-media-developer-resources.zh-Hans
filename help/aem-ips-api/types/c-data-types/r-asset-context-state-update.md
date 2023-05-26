---
title: AssetContextStateUpdate
description: 为与资产关联的发布上下文设置一组新的发布状态标记。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: ecbadafc-e77d-4c7e-a3d5-31c2b2a9b2ea
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 6%

---

# [!DNL AssetContextStateUpdate]{#assetcontextstateupdate}

为与资产关联的发布上下文设置一组新的发布状态标记。

**参数**

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 处理要更新的资产。 |
| contextStateUpdateArray | `types:ContextStateUpdateArray` | 要更新的资源的发布联系状态数组。 |
