---
description: 默认图像文件后缀。 如果路径不包含文件后缀，则附加到目录路径（或目录掩码路径）字段值
solution: Experience Manager
title: DefaultExt
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 43b3e5b8-6374-458d-8503-8e04c8c84233
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---

# DefaultExt{#defaultext}

默认图像文件后缀。 如果路径不包含文件后缀，则附加到目录：:Path（或目录：:MaskPath）字段值

文件后缀由句点和一个或多个字符组成，这些字符介于句点和字符串末尾之间。 如果路径未解析为目录条目，并且最后一个路径元素不包含文件后缀，后缀将附加到http路径。

## 属性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文本字符串。 必须包含前导“。” 和一个或多个字符。

## 默认 {#section-1194c36ffe0748c5b9ff7d732a506588}

从`default::DefaultExt`继承（如果未定义）。 如果已定义但为空，则使用此目录时，不会对图像名称应用默认后缀。

## 另请参阅 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
