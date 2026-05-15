---
description: 更新与图像资产关联的图像字段。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
TQID: 'https://experienceleague.adobe.com/IsOZvDzvJTa0KJfUkYblEln9Qrx7nQm79FEEbnFVjiw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 56
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

更新与图像资产关联的图像字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 资产句柄。 |
| [!DNL resolution] | `xsd:double` | 图像分辨率（像素/英寸）。 |
| [!DNL anchorX] | `xsd:int` | X轴图像锚点。 |
| [!DNL anchorY] | `xsd:int` | Y轴图像锚点。 |
| [!DNL userData] | `xsd:string` | `userData`元数据字段的值，该字段已发布到图像服务用户数据目录字段。 |
