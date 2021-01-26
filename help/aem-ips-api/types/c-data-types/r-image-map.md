---
description: 目标以在浏览器中执行单击操作。
seo-description: 目标以在浏览器中执行单击操作。
seo-title: 图像映射
solution: Experience Manager
title: 图像映射
topic: Dynamic Media Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 13%

---


# 图像映射{#imagemap}

目标以在浏览器中执行单击操作。

始终与图像关联。 您可以从`ImageInfo`获得`ImageMap`目标。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 图像映射手柄。 |
| `*`name`*` | `xsd:string` | 图像映射名称。 |
| `*`地区`*` | `xsd:string` | 图像地图坐标。 格式基于HTML `<area>`标记属性。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`标签中的其他属性，包括`href` URL。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]值。 |
| `*`position`*` | `xsd:string` | 以HTML `<area>`元素的[!DNL coords]属性的格式放置。 示例: `coords ="0,0,84,128"`. |
| `*`已启用`*` | `xsd:boolean` | 如果启用图像映射，则为True。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |

