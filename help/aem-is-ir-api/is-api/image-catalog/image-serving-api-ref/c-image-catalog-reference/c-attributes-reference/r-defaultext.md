---
description: 默认图像文件后缀。 如果路径不包含文件后缀，则附加到目录Path（或目录MaskPath）字段值
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---

# DefaultExt{#defaultext}

默认图像文件后缀。 如果路径不包含文件后缀，则附加到catalog：：Path （或catalog：：MaskPath）字段值

文件后缀包含一个句点，以及介于句点和字符串结尾之间的一个或多个字符。 如果路径未解析为目录条目，并且最后一个路径元素不包含文件后缀，则后缀将附加到http路径中。

## 属性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文本字符串。 必须包含前导“。” 和一个或多个字符。

## 默认 {#section-1194c36ffe0748c5b9ff7d732a506588}

如果未定义，则从`default::DefaultExt`继承。 如果已定义但为空，则在使用此目录时，默认后缀不会应用于图像名称。

## 另请参阅 {#section-d7c408b979844643adff8258f500eb7c}

[目录：：Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ， [目录：：MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
