---
title: TiffEncoding
description: 编码格式TIFF。 指定TIFF图像的压缩格式（实际上是fmt=命令的第三个值的默认值）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 4%

---

# TiffEncoding{#tiffencoding}

编码格式TIFF。 指定TIFF图像的压缩格式（实际上是`fmt=`命令的第三个值的默认值）。

设置为`0`表示无压缩，`1`表示LZW，`2`表示deflate (ZIP)，`3`表示JPEG压缩。

## 属性 {#section-469f5a1225464542866f5353edd92db3}

枚举。

## 默认 {#section-a3c5152a9f464e4987ed7c05d35b1169}

如果未定义或为空，则从`default::TiffEncoding`继承。

## 另请参阅 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)
