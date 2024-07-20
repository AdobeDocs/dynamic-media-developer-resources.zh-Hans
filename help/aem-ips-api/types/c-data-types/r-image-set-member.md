---
description: 属于图像集的Assets。
solution: Experience Manager
title: ImageSetMember
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: f0857d98-be79-40a6-8a84-c2c7b4c423c5
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 7%

---

# [!DNL ImageSetMember]{#imagesetmember}

属于图像集的Assets。

页面重置意味着[!DNL eCatalog]应开始一个新页面。 `RenderSet`指示它是`RenderSet`样本的一部分。 对于`eCatalog`和`RenderSet`集，该值强制为`true`。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| asset | `type:Asset` | 图像集数组中的Assets。 |
| pageReset | `xsd:boolean` | 开始新页面。 设置被忽略，`eCatalog`和`RenderSet`集的值强制为`true`。 |
