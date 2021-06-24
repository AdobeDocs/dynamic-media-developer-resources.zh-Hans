---
description: 属于图像集的资产。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic，SDK/API，图像集
role: Developer,Administrator
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 6%

---

# ImageSetMember{#imagesetmember}

属于图像集的资产。

页面重置表示[!DNL eCatalog]应开始新页面。 `RenderSet` 表示它是色板的一 `RenderSet` 部分。对于`eCatalog`和`RenderSet`集，该值会强制设置为`true`。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`asset`*` | `type:Asset` | 图像集数组中的资产。 |
| `*`pageReset`*` | `xsd:boolean` | 启动新页面。 将忽略设置，并将`eCatalog`和`RenderSet`集的值强制设置为`true`。 |
