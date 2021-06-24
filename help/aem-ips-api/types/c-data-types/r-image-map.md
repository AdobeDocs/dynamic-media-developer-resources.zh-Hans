---
description: 定位以在浏览器中执行点击操作。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 12%

---

# 图像映射{#imagemap}

定位以在浏览器中执行点击操作。

始终与图像关联。 您可以从`ImageInfo`获取`ImageMap`目标。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 图像映射句柄。 |
| `*`name`*` | `xsd:string` | 图像映射名称。 |
| `*`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标记属性。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`标记中的其他属性，包括`href` URL。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]值。 |
| `*`position`*` | `xsd:string` | 以HTML `<area>`元素[!DNL coords]属性的格式放置。 示例: `coords ="0,0,84,128"`. |
| `*`已启用`*` | `xsd:boolean` | 如果启用了图像映射，则为True。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |
