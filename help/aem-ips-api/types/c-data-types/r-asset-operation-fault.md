---
title: 资产操作出错
description: 包含有关在批处理资源操作期间生成的警告或错误条件的信息。 代码和原因字段对应于因等效的非批处理操作而引发的错误消息字段。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 92
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

