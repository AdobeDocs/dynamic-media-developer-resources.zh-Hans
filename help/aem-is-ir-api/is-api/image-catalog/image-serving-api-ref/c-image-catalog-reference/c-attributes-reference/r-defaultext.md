---
description: 默认图像文件后缀。 如果路径不包含文件后缀，则附加到目录路径（或目录蒙版路径）字段值
seo-description: 默认图像文件后缀。 如果路径不包含文件后缀，则附加到目录路径（或目录蒙版路径）字段值
seo-title: DefaultExt
solution: Experience Manager
title: DefaultExt
topic: Scene7 Image Serving - Image Rendering API
uuid: aa245d18-15cc-41cb-a49d-757d74fe6231
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# DefaultExt{#defaultext}

默认图像文件后缀。 附加到目录：:Path（或catalog:::MaskPath）字段值（如果路径不包含文件后缀）

文件后缀由句点和字符串的句点与结尾之间的一个或多个字符组成。 如果路径未解析为目录条目，并且如果最后一个路径元素不包含文件后缀，则后缀将附加到http路径。

## 属性 {#section-b024e6450b414ccc8b83a48a3b4e00f9}

文本字符串。 必须包含前导&#39;.&#39; 和一个或多个字符。

## 默认 {#section-1194c36ffe0748c5b9ff7d732a506588}

如果未定义， `default::DefaultExt` 则从中继承。 如果已定义但为空，则在使用此目录时，不会将默认后缀应用于图像名称。

## 另请参阅 {#section-d7c408b979844643adff8258f500eb7c}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md)
