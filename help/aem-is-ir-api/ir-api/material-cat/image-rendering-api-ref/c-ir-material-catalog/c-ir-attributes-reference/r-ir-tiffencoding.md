---
description: TIFF编码格式。 指定TIFF图像的压缩格式（实际上是fmt=命令的第三个值的默认值）。
seo-description: TIFF编码格式。 指定TIFF图像的压缩格式（实际上是fmt=命令的第三个值的默认值）。
seo-title: TiffEncoding
solution: Experience Manager
title: TiffEncoding
topic: Scene7 Image Serving - Image Rendering API
uuid: b9f672f8-d759-4248-8588-9fe46db1645f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TiffEncoding{#tiffencoding}

TIFF编码格式。 指定TIFF图像的压缩格式（实际上是fmt=命令的第三个值的默认值）。

设置为0表示无压缩，设置为1表示LZW，设置为2表示deflate(ZIP)，设置为3表示JPEG压缩。

## 属性 {#section-469f5a1225464542866f5353edd92db3}

枚举。

## 默认 {#section-a3c5152a9f464e4987ed7c05d35b1169}

如果未定义 `default::TiffEncoding` 或为空，则从中继承。

## 另请参阅 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
