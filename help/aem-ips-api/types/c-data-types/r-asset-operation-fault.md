---
title: 资产操作出错
description: 包含有关在批处理资源操作期间生成的警告或错误条件的信息。 代码和原因字段对应于因等效的非批处理操作而引发的错误消息字段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

包含有关在批处理资源操作期间生成的警告或错误条件的信息。 代码和原因字段对应于因等效的非批处理操作而引发的错误消息字段。

语法

## 参数 {#section-c906f052f43e4785ba46d92b514b0923}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 失败的操作的资产句柄。 |
| 代码 | `xsd:int` | 操作错误代码。 |
| 原因 | `xsd:string` | 错误描述或原因。 |
