---
description: 属于图像集的资产。
seo-description: 属于图像集的资产。
seo-title: ImageSetMember
solution: Experience Manager
title: ImageSetMember
topic: Scene7 Image Production System API
uuid: bd013609-aed7-4c85-80f9-16be7fce99a3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageSetMember{#imagesetmember}

属于图像集的资产。

页面重置表示应 [!DNL eCatalog] 开始新页面。 `RenderSet` 表示它是色板的一 `RenderSet` 部分。 该值将强制 `true` 用于 `eCatalog` 和 `RenderSet` 集。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`asset`*` | `type:Asset` | 图像集阵列中的资源。 |
| ` *`pageReset`*` | `xsd:boolean` | 开始新页面。 将忽略设置，并强制将值用 `true` 于 `eCatalog` 和 `RenderSet` 集。 |

