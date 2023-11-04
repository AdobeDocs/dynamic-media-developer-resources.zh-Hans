---
description: 图像文件路径。
solution: Experience Manager
title: 路径
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 4%

---

# 路径{#path}

图像文件路径。

与此目录记录关联的源图像文件的相对或绝对路径和名称。 服务器使用管理源数据中描述的路径解析规则来查找数据文件。

## 属性 {#path-properties}

文本字符串。 图像记录需要，模板记录可能为空。 如果已指定，则必须是有效的相对或绝对图像服务器文件路径。 如果没有文件后缀，则会附加attribute：：DefaultExt。

## 支持的图像文件格式 {#path-supported-image-file-formats}

有关支持的文件格式的完整列表，请参阅图像转换器(IC)实用程序的说明。

当使用Dynamic Media金字塔TIFF(PTIFF)多分辨率格式时，需要多个不同分辨率的图像数据的应用程序性能最佳。 IC实用程序用于从任何支持的图像格式创建PTIFF图像。

## 默认 {#path-default}

无。

## 另请参阅 {#path-seealso}

[集成电路实用程序](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ， [属性：：RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ， [attribute：：DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ， [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
