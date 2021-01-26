---
description: 图像文件路径。
solution: Experience Manager
title: 路径
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# 路径{#path}

图像文件路径。

与此目录记录关联的源图像文件的相对或绝对路径和名称。 服务器使用管理源数据中所述的路径解析规则查找数据文件。

## 属性 {#path-properties}

文本字符串。 图像记录必需，模板记录可为空。 如果指定，则它必须是有效的相对或绝对图像服务器文件路径。 属性：：如果不存在文件后缀，则附加DefaultExt。

## 支持的图像文件格式{#path-supported-image-file-formats}

有关所支持文件格式的完整列表，请参阅图像转换器(IC)实用程序的说明。

使用Dynamic Media金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 IC实用程序用于从任何支持的图像格式创建PTIFF图像。

## 默认 {#path-default}

无。

## 另请参阅 {#path-seealso}

[IC实用程](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) 序， [属性：:RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ，属 [性：:DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->