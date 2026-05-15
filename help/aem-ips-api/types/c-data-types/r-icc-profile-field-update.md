---
description: 更新ICC配置文件属性的信息。
solution: Experience Manager
title: IccProfileFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b988a430-8ed6-456b-b37b-b4185c5d3b32
TQID: 'https://experienceleague.adobe.com/-HbYlEjS3SdM9Sr0jgaQdve1H9wr7e51oAvAy-C-0vI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 52
ht-degree: 9%

---

# [!DNL IccProfileFieldUpdate]{#iccprofilefieldupdate}

更新ICC配置文件属性的信息。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 要更新的ICC配置文件资产的句柄。 |
| [!DNL class] | `xsd:string` | 配置文件分类（有关值，请参阅“配置文件分类”）。 |
| 色彩空间 | `xsd:string` | 配置文件颜色空间（有关值，请参阅“颜色空间”）。 |
| pcstype | `xsd:string` | 配置文件连接空间（有关值，请参阅“颜色空间”）。 |
