---
description: 包含有关批处理资产操作期间生成的警告或错误条件的信息。 代码字段和原因字段对应于为对等非批处理操作引发的故障消息字段。
seo-description: 包含有关批处理资产操作期间生成的警告或错误条件的信息。 代码字段和原因字段对应于为对等非批处理操作引发的故障消息字段。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

包含有关批处理资产操作期间生成的警告或错误条件的信息。 代码字段和原因字段对应于为对等非批处理操作引发的故障消息字段。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失败操作的资产句柄。 |
| `*`代码`*` | `xsd:int` | 操作错误代码。 |
| `*`原因`*` | `xsd:string` | 错误描述或原因。 |

