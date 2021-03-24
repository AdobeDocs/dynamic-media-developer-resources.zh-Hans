---
description: 包含有关批处理资产操作期间生成的警告或错误条件的信息。 代码字段和原因字段对应于为对等非批处理操作引发的故障消息字段。
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic，SDK/API，资产管理
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

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

