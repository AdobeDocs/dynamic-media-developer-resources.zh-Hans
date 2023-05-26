---
description: 更新与图像资源关联的图像字段。
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 8%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

更新与图像资源关联的图像字段。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| assetHandle | `xsd:string` | 资源句柄。 |
| [!DNL resolution] | `xsd:double` | 图像分辨率（像素/英寸）。 |
| [!DNL anchorX] | `xsd:int` | X轴图像锚点。 |
| [!DNL anchorY] | `xsd:int` | Y轴图像锚点。 |
| [!DNL userData] | `xsd:string` | 值 `userData` 元数据字段，已发布到图像服务用户数据目录字段。 |
