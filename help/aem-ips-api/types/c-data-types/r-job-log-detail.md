---
description: 作业日志信息。
solution: Experience Manager
title: 作业日志详细信息
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 8%

---

# [!DNL JobLogDetail]{#joblogdetail}

作业日志信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| logMessage | `xsd:string` | 作业日志中的消息。 |
| logType | `xsd:string` | 作业日志文件类型。 |
| 资产名称 | `xsd:string` | 作业日志中的资源名称（可选）。 |
| 资产类型 | `xsd:string` | 资源类型的选择。 |
| assetHandle | `xsd:string` | 作业日志中引用的资产句柄。 |
| 辅助阵列 | `types:JobLogDetailAuxArray` | 提供上述五种作业日志类型以外的其他详细作业日志信息。 |
