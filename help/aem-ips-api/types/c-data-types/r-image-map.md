---
description: 浏览器中点击操作的目标。
solution: Experience Manager
title: 图像映射
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

浏览器中点击操作的目标。

始终与图像关联。 您可以从`ImageInfo`获取`ImageMap`目标。

## 参数 {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名称 | 类型 | 说明 |
|---|---|---|
| imageMapHandle | `xsd:string` | 图像映射句柄。 |
| [!DNL name] | `xsd:string` | 图像映射名称。 |
| [!DNL region] | `xsd:string` | 图像映射坐标。 格式基于HTML`<area>`标记属性。 |
| [!DNL action] | `xsd:string` | 要包含在HTML`<area>`标记中的其他属性，包括`href` URL。 |
| shapeType | `xsd:boolean` | [!DNL RegionShape]值。 |
| [!DNL position] | `xsd:string` | 以HTML`<area>`元素的[!DNL coords]属性的格式表示的位置。 例如： `coords ="0,0,84,128"`。 |
| [!DNL enabled] | `xsd:boolean` | 如果启用了图像映射，则为True。 |
| lastModified | `xsd:dateTime` | 上次修改图像映射的日期和时间。 |
