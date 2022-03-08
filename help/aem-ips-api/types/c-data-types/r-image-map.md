---
description: 定位以在浏览器中执行点击操作。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

---

# 图像映射{#imagemap}

定位以在浏览器中执行点击操作。

始终与图像关联。 你可以 `ImageMap` 目标 `ImageInfo`.

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 图像映射句柄。 |
| name | `xsd:string` | 图像映射名称。 |
| 地区 | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>` 标记属性。 |
| 操作 | `xsd:string` | 要包含在HTML中的其他属性 `<area>` 标记，包括 `href` URL。 |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] 值。 |
| position | `xsd:string` | 以HTML格式放置 `<area>` 元素 [!DNL coords] 属性。 示例: `coords ="0,0,84,128"`. |
| 已启用 | `xsd:boolean` | 如果启用了图像映射，则为True。 |
| lastModified | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |
