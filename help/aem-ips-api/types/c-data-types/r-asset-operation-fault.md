---
description: 包含有关在批处理资产操作过程中生成的警告或错误条件的信息。 代码和原因字段与为对等非批处理操作引发的故障消息字段相对应。
seo-description: 包含有关在批处理资产操作过程中生成的警告或错误条件的信息。 代码和原因字段与为对等非批处理操作引发的故障消息字段相对应。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Dynamic Media Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---


# AssetOperationFault{#assetoperationfault}

包含有关在批处理资产操作过程中生成的警告或错误条件的信息。 代码和原因字段与为对等非批处理操作引发的故障消息字段相对应。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 失败的操作的资产句柄。 |
| `*`代码`*` | `xsd:int` | 操作故障代码。 |
| `*`原因`*` | `xsd:string` | 错误描述或原因。 |

