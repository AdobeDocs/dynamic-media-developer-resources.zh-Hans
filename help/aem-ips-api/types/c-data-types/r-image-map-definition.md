---
description: 目标在浏览器中单击操作的定义。
seo-description: 目标在浏览器中单击操作的定义。
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Dynamic Media Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

目标在浏览器中单击操作的定义。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 图像映射定义的名称。 |
| `*`shapeType`*` | `xsd:string` | 区域形状值之一。 |
| `*`地区`*` | `xsd:string` | 图像地图坐标。 格式基于HTML `<area>`标签属性。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`标签中的其他属性，包括`href` URL。 |
| `*`已启用`*` | `xsd:boolean` | 如果启用图像映射，则返回true。 |

