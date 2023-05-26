---
description: 目录记录标识符
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Id {#id}

用于查找图像数据文件中的记录的索引键值 [!DNL Platform Server].

通常，如果一个SKU具有多个图像，则使用简短且唯一的图像标识符（如SKU编号），并可能包含某种类型的图像后缀。 也可能是更复杂的字符串，看起来更像文件路径，以支持通过图像服务轻松地对网站进行追溯。

## 属性 {#id-properties}

文本字符串。 必需. 图像数据表的主索引键。 每个目录：：Id值在表中必须是唯一的。

## 默认 {#id-default}

无。

## 另请参阅 {#id-seealso}

[attribute：：RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
