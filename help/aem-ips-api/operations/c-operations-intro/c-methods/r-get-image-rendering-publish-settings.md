---
description: 仅供内部使用。 请参阅图像渲染材料目录参考目录属性部分。
seo-description: 仅供内部使用。 请参阅图像渲染材料目录参考目录属性部分。
seo-title: getImageRenderingPublishSettings
solution: Experience Manager
title: getImageRenderingPublishSettings
uuid: b1c253b5-febe-4dc7-95a1-a5f4789030e7
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 13%

---


# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

仅供内部使用。 请参阅图像渲染材料目录参考目录属性部分。

语法

## 授权用户类型{#section-1097e0563c61480a8e97822dc3527070}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-4f2cb8c589384816bb2525654ec49963}

**输入(getImageRenderingPublishSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 要获取其图像渲染发布设置的公司的句柄。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 处理发布上下文。 |

**输出(getImageRenderingPublishSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`publishSettingsArray`*` | `type:ConfigSettingArray` | 是 | 图像渲染发布设置。 |

