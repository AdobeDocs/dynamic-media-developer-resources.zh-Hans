---
description: 属于图像集的资产。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 7%

---

# ImageSetMember{#imagesetmember}

属于图像集的资产。

页面重置表示 [!DNL eCatalog] 应启动新页面。 `RenderSet` 表示它是 `RenderSet` 色板。 该值将强制 `true` 表示 `eCatalog` 和 `RenderSet` 设置。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| asset | `type:Asset` | 图像集数组中的资产。 |
| pageReset | `xsd:boolean` | 启动新页面。 将忽略设置，并将值强制设置为 `true` 表示 `eCatalog` 和 `RenderSet` 设置。 |
