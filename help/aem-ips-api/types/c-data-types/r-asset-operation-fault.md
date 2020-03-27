---
description: 包含有关在批资产操作过程中生成的警告或错误条件的信息。 代码字段和原因字段与为对等非批处理操作而引发的故障消息字段相对应。
seo-description: 包含有关在批资产操作过程中生成的警告或错误条件的信息。 代码字段和原因字段与为对等非批处理操作而引发的故障消息字段相对应。
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetOperationFault{#assetoperationfault}

包含有关在批资产操作过程中生成的警告或错误条件的信息。 代码字段和原因字段与为对等非批处理操作而引发的故障消息字段相对应。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | 失败的操作的资产句柄。 |
| ` *`代码`*` | `xsd:int` | 操作故障代码。 |
| ` *`原因`*` | `xsd:string` | 错误描述或原因。 |

