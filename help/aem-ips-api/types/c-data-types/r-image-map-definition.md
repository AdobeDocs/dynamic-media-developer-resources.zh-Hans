---
description: 目标定义浏览器中的单击操作。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 11%

---


# ImageMapDefinition{#imagemapdefinition}

目标定义浏览器中的单击操作。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`name`*` | `xsd:string` | 图像映射定义的名称。 |
| `*`shapeType`*` | `xsd:string` | 区域形状值之一。 |
| `*`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标签属性。 |
| `*`操作`*` | `xsd:string` | HTML `<area>`标签中要包含的其他属性，包括`href` URL。 |
| `*`已启用`*` | `xsd:boolean` | 如果启用了图像映射，则返回true。 |

