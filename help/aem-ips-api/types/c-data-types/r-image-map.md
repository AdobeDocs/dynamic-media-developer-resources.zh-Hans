---
description: 浏览器中点击操作的Target。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 6%

---

# [!DNL ImageMap]{#imagemap}

浏览器中点击操作的Target。

始终与图像关联。 您可以获得一个 `ImageMap` 目标来源 `ImageInfo`.

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 图像映射句柄。 |
| [!DNL name] | `xsd:string` | 图像映射名称。 |
| [!DNL region] | `xsd:string` | 图像映射坐标。 格式基于HTML `<area>` 标记属性。 |
| [!DNL action] | `xsd:string` | 要包含在HTML中的其他属性 `<area>` 标记，包括 `href` URL。 |
| shapetype | `xsd:boolean` | A [!DNL RegionShape] 值。 |
| [!DNL position] | `xsd:string` | 在HTML格式中的位置 `<area>` 元素的 [!DNL coords] 属性。 示例: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | 如果启用了图像映射，则为True。 |
| lastModified | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |
