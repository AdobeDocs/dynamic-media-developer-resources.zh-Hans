---
description: 浏览器中单击操作的目标定义。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic，SDK/API
role: Developer,Administrator
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 11%

---

# ImageMapDefinition{#imagemapdefinition}

浏览器中单击操作的目标定义。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 图像映射定义的名称。 |
| `*`shapeType`*` | `xsd:string` | 区域形状值之一。 |
| `*`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标记属性。 |
| `*`操作`*` | `xsd:string` | 要包含在HTML `<area>`标记中的其他属性，包括`href` URL。 |
| `*`已启用`*` | `xsd:boolean` | 如果启用了图像映射，则返回true。 |
