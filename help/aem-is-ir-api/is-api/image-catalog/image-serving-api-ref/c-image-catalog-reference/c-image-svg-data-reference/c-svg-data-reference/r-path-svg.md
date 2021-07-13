---
description: 路径
solution: Experience Manager
title: 路径
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f2d17309-c4d0-477f-a8d8-b40f05a1a60b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 5%

---

# 路径{#path}

服务器使用[管理源数据](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)中描述的路径解析规则来查找数据文件。

## 属性 {#section-72d9edc532ad43349afcb4df22e1c692}

文本字符串。 图像和SVG记录必需，对于模板记录，可能为空。 如果已指定，则必须是有效的相对或绝对图像服务器文件路径。 属性：：如果不存在文件后缀，则会附加DefaultExt。

## 支持的图像文件格式 {#section-8d6443c883aa48aaa00316fe9661aaa8}

有关支持的图像文件格式的完整列表，请参阅图像转换器(IC)实用程序的说明。

使用Dynamic Media金字塔TIFF(PTIFF)多分辨率格式时，如果应用程序需要多种不同分辨率的图像数据，则其效果会最佳。 IC实用程序用于根据任何受支持的图像格式创建PTIFF图像。

## 默认 {#section-82dad83ec3f84ae8bf2f850b4139f63e}

无。

## 另请参阅 {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[IC实用程序](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [属性：:RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [属性：:DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0),  [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
