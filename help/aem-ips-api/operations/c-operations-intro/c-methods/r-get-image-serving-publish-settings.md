---
description: 仅供内部使用。 用户应该参阅图像提供图像目录引用 — 属性引用一节。
solution: Experience Manager
title: getImageServingPublishSettings
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: ab7b5df6-58fb-4111-be9c-76901534d167
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# getImageServingPublishSettings{#getimageservingpublishsettings}

仅供内部使用。 用户应该参阅图像提供图像目录引用 — 属性引用一节。

语法

## 授权用户类型 {#section-49b7b277ba1748499121a0e90996458c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 参数 {#section-79f0d54acd604ad2a5c96679334f2424}

**输入(getImageServingPublishSettingsParam)**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 具有图像服务发布设置的公司的句柄。 |
| `*`contextHandle`*` | `xsd:string` | 是 | 处理发布上下文。 |

**输出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| `*`publishSettingArray`*` | `xsd:string` | 是 | 图像服务器发布设置的数组。 |
