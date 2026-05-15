---
description: 仅供内部使用。 请参阅图像渲染材质目录Reference-Catalog属性部分。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
TQID: 'https://experienceleague.adobe.com/-zBv9N9COcH6KjyHfgjYF4TXblntNiZMVBB6nr-oe2w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

仅供内部使用。 请参阅图像渲染材质目录Reference-Catalog属性部分。

语法

## 授权用户类型 {#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-4f2cb8c589384816bb2525654ec49963}

**输入(getImageRenderingPublishSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 您希望获取其图像渲染发布设置的公司的句柄。 |
| contextHandle | `xsd:string` | 是 | 处理发布上下文。 |

**输出(getImageRenderingPublishSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | 是 | 图像渲染发布设置。 |
