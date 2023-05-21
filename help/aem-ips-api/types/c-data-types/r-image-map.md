---
description: 瀏覽器中點按動作的Target。
solution: Experience Manager
title: 影像地圖
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 6%

---

# [!DNL ImageMap]{#imagemap}

瀏覽器中點按動作的Target。

一律與影像相關聯。 您可以取得 `ImageMap` 目標來源 `ImageInfo`.

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 影像地圖控點。 |
| [!DNL name] | `xsd:string` | 影像地圖名稱。 |
| [!DNL region] | `xsd:string` | 影像地圖座標。 格式取決於HTML `<area>` 標籤屬性。 |
| [!DNL action] | `xsd:string` | 要包含在HTML中的其他屬性 `<area>` 標籤，包括 `href` URL。 |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] 值。 |
| [!DNL position] | `xsd:string` | 在HTML格式中的位置 `<area>` 元素的 [!DNL coords] 屬性。 示例: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 如果啟用影像地圖，則為True。 |
| lastModified | `xsd:dateTime` | 上次修改影像地圖的日期與時間。 |
