---
description: 浏览器中点击操作的目标定义。
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

浏览器中点击操作的目标定义。

语法

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| 名称 | `xsd:string` | 图像映射定义的名称。 |
| shapetype | `xsd:string` | 区域形状值之一。 |
| 地区 | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>` 标记属性。 |
| 操作 | `xsd:string` | 要包含在HTML中的其他属性 `<area>` 标记，包括 `href` URL。 |
| 已启用 | `xsd:boolean` | 如果启用了图像映射，则为True。 |
