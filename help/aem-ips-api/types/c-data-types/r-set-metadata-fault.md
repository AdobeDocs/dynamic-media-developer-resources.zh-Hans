---
description: 在batchSetAssetMetadata操作中使用更新的警告或错误详细信息。
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
TQID: 'https://experienceleague.adobe.com/kqC7eTmOZHNIYAn8yTKr-q-rJMQMzqBC9moArFK9no4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 58
ht-degree: 12%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

在batchSetAssetMetadata操作中使用更新的警告或错误详细信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 未能成功设置其元数据的资源。 |
| fieldHandle | `xsd:string` | 设置值失败的元数据字段的句柄。 |
| 代码 | `xsd:int` | 错误代码。 |
| 原因 | `xsd:string` | 错误描述（纯文本）。 |

