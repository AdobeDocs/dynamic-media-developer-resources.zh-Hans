---
description: 目标浏览器中的单击操作。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic，SDK/API
role: 开发人员，管理员
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 12%

---


# 图像映射{#imagemap}

目标浏览器中的单击操作。

始终与图像关联。 您可以从`ImageInfo`获得`ImageMap`目标。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | 图像映射手柄。 |
| `*`name`*` | `xsd:string` | 图像映射名称。 |
| `*`地区`*` | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>`标签属性。 |
| `*`操作`*` | `xsd:string` | HTML `<area>`标签中要包含的其他属性，包括`href` URL。 |
| `*`shapeType`*` | `xsd:boolean` | [!DNL RegionShape]值。 |
| `*`position`*` | `xsd:string` | 以HTML `<area>`元素的[!DNL coords]属性的格式放置。 示例: `coords ="0,0,84,128"`. |
| `*`已启用`*` | `xsd:boolean` | 如果启用了图像映射，则返回true。 |
| `*`lastModified`*` | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |

