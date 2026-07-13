---
description: 将查看器配置设置附加到资源。 这些可以是查看器预设或查看器的源资产。
solution: Experience Manager
title: setViewerConfigSettings
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: 6b70f2c3-c98b-455f-b453-bb797744dadc
TQID: 'https://experienceleague.adobe.com/MX6dj-7j6HfNSISaWFheorOZYVnszSY24OuuUGdKvPA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 12%

---

# setViewerConfigSettings{#setviewerconfigsettings}

将查看器配置设置附加到资源。 这些可以是查看器预设或查看器的源资产。

语法

## 授权用户类型 {#section-81c429ba9f4c4359986a30ea7ebea8d2}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-bcc8c83cc84141e8b1341be9133e8511}

**输入(setViewerConfigSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 处理公司。 |
| assetHandle | `xsd:string` | 是 | 资产句柄。 |
| 名称 | `xsd:string` | 是 | 资源名称。 |
| 类型 | `xsd:string` | 是 | 要将查看器配置应用于的资源类型。 |
| configSettingArray | `types:ConfigSettingArray` | 是 | `ConfigSettings`的数组已应用于资源。 |

**输出(setViewerConfigSettingsParam)**

IPS API不返回此操作的响应。

