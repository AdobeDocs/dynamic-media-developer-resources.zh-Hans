---
description: 仅供内部使用。 用户应该参阅图像服务图像目录参考——属性参考部分。
seo-description: 仅供内部使用。 用户应该参阅图像服务图像目录参考——属性参考部分。
seo-title: getImageServingPublishSettings
solution: Experience Manager
title: getImageServingPublishSettings
topic: Scene7 Image Production System API
uuid: 2f00198d-0262-430b-8ac5-80f52adcff67
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getImageServingPublishSettings{#getimageservingpublishsettings}

仅供内部使用。 用户应该参阅图像服务图像目录参考——属性参考部分。

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
| ` *`companyHandle`*` | `xsd:string` | 是 | 具有图像服务发布设置的公司的句柄。 |
| ` *`contextHandle`*` | `xsd:string` | 是 | 处理发布上下文。 |

**输出**

| 名称 | 类型 | 必需 | 说明 |
|---|---|---|---|
| ` *`publishSettingArray`*` | `xsd:string` | 是 | 图像服务器发布设置的阵列。 |

