---
description: 目录记录标识符
solution: Experience Manager
title: Id
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 7%

---

# Id {#id}

Platform Server查找图像数据文件中记录时所依据的索引键值。

通常，如果SKU具有多个图像，则是一个简短且唯一的图像标识符，例如SKU号，可能带有某种图像后缀。 可能还是一个更复杂的字符串，看起来更像文件路径，可支持使用图像服务轻松进行网站的重新拟合。

## 属性 {#id-properties}

文本字符串。 必需. 图像数据表的主索引键。 每个目录：:Id值在表中必须唯一。

## 默认 {#id-default}

无。

## 另请参阅 {#id-seealso}

[属性：:RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
