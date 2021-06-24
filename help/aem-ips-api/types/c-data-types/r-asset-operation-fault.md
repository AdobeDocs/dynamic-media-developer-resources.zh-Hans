---
description: 包含有关批资产操作期间生成的警告或错误条件的信息。 代码和原因字段对应于为等效的非批处理操作而引发的故障消息字段。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic，SDK/API，资产管理
role: Developer,Administrator
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

包含有关批资产操作期间生成的警告或错误条件的信息。 代码和原因字段对应于为等效的非批处理操作而引发的故障消息字段。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失败操作的资产句柄。 |
| `*`代码`*` | `xsd:int` | 操作故障代码。 |
| `*`原因`*` | `xsd:string` | 故障描述或原因。 |
