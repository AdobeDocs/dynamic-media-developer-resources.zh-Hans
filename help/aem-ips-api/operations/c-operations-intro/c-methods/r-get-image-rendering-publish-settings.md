---
description: 仅供内部使用。 请参阅图像渲染材料目录引用目录属性部分。
solution: Experience Manager
title: getImageRenderingPublishSettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 152dfd61-2fba-47b4-8e69-fbbc8fb57f87
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 17%

---

# getImageRenderingPublishSettings{#getimagerenderingpublishsettings}

仅供内部使用。 请参阅图像渲染材料目录引用目录属性部分。

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

**Output(getImageRenderingPublishSettingsReturn)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| publishSettingsArray | `type:ConfigSettingArray` | 是 | 图像渲染发布设置。 |
