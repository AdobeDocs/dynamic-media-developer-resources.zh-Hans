---
description: 获取与指定资源关联的所有查看器配置设置。
solution: Experience Manager
title: getViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: c0438238-8aab-4478-926a-fc0e11732fc1
TQID: 'https://experienceleague.adobe.com/GeSAS1EP7Q6EgsQltyC-TVnxS0zusuKxKs6QL8wfLWw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 22%

---

# getViewerConfigSettings{#getviewerconfigsettings}

获取与指定资源关联的所有查看器配置设置。

语法

## 授权用户类型 {#section-05c3ea8f7d2d42c6bf7af63e03f457a9}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-7d06abf3d707494c8a1270c7fa1477f1}

**输入(getViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 处理公司。 |
| assetHandle | `xsd:string` | 是 | 处理资源。 |

**输出(getViewerCoinfigSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| 类型 | `xsd:string` | 是 | 配置设置应用于的查看器类型。 |
| configSettingsArray | `types:ConfigSettingsArray` | 是 | 查看器配置设置数组。 |

