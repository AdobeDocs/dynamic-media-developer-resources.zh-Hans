---
description: 目标以在浏览器中执行单击操作。
seo-description: 目标以在浏览器中执行单击操作。
seo-title: 图像映射
solution: Experience Manager
title: 图像映射
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 图像映射{#imagemap}

目标以在浏览器中执行单击操作。

始终与图像关联。 你可以从中 `ImageMap` 获得目标 `ImageInfo`。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | 图像映射手柄。 |
| ` *`名称`*` | `xsd:string` | 图像映射名称。 |
| ` *`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML标签 `<area>` 属性。 |
| ` *`操作`*` | `xsd:string` | 要包含在HTML标记中的其 `<area>` 他属性，包括 `href` URL。 |
| ` *`shapeType`*` | `xsd:boolean` | 一个 [!DNL RegionShape] 值。 |
| ` *`位置`*` | `xsd:string` | 以HTML元素属性的格 `<area>` 式放置 [!DNL coords] 位置。 示例: `coords ="0,0,84,128"`. |
| ` *`已启用`*` | `xsd:boolean` | 如果启用了图像映射，则返回true。 |
| ` *`lastModified`*` | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |

