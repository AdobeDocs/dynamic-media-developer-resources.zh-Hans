---
description: 目标浏览器中单击操作的定义。
seo-description: 目标浏览器中单击操作的定义。
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Scene7 Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ImageMapDefinition{#imagemapdefinition}

目标浏览器中单击操作的定义。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| ` *`名称`*` | `xsd:string` | 图像映射定义的名称。 |
| ` *`shapeType`*` | `xsd:string` | 区域形状值之一。 |
| ` *`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML标签 `<area>` 属性。 |
| ` *`操作`*` | `xsd:string` | 要包含在HTML标记中的其 `<area>` 他属性，包括 `href` URL。 |
| ` *`已启用`*` | `xsd:boolean` | 如果图像映射处于启用状态，则返回true。 |

