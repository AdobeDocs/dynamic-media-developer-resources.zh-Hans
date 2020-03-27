---
description: 静态内容数据根路径。 此图像目录静态内容数据的根文件夹的绝对路径或相对路径段。
seo-description: 静态内容数据根路径。 此图像目录静态内容数据的根文件夹的绝对路径或相对路径段。
seo-title: StaticContentRootPath
solution: Experience Manager
title: StaticContentRootPath
topic: Scene7 Image Serving - Image Rendering API
uuid: f1c0a54c-8b2c-4953-a3b7-180d231840db
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# StaticContentRootPath{#staticcontentrootpath}

静态内容数据根路径。 此图像目录静态内容数据的根文件夹的绝对路径或相对路径段。

有关服 [务器根路径的其他信息](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) ，请参阅管理源数据。

## 属性 {#section-f8e3986096294b36948d43aafdc3e795}

文本字符串。 必须为空、有效的相对文件路径段或绝对路径。 不应包括前导和尾部路径元素分隔符。

## 默认 {#section-0f741f90fd8d4758a43162c2b5c8a3a3}

如果未定义， `default::StaticContentsRootPath` 则从中继承。 如果已定义但为空，则不会贡献到源文件根路径。

## 另请参阅 {#section-9af8846d20d242789df67877f84ed8a7}

[PS::staticContent.rootPaths](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-staticcontentrootpath.md#reference-a2b5368d078349828d282357681bb2a5) , [管理源数据](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173)
