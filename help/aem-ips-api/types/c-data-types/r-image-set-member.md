---
description: 属于图像集的资产。
seo-description: 属于图像集的资产。
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---


# ImageSetMember{#imagesetmember}

属于图像集的资产。

页面重置表示[!DNL eCatalog]应开始新页面。 `RenderSet` 表示它是色板的一 `RenderSet` 部分。对于`eCatalog`和`RenderSet`集，该值被强制为`true`。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 图像集数组中的资源。 |
| `*`pageReset`*` | `xsd:boolean` | 开始新页面。 将忽略设置，并将`eCatalog`和`RenderSet`集的值强制为`true`。 |

