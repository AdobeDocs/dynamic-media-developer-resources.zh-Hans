---
title: TiffEncoding
description: TIFF编码格式。 指定TIFF图像的压缩格式（实际上是fmt=命令的第三个值的默认值）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6a6fa8f5-4497-438d-914c-3f6d4c08ef09
TQID: 'https://experienceleague.adobe.com/lSR8V09ooHaKYbD-GFAiuK-QcRJBKkXkVMTKy7Oj2e0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 4%

---

# TiffEncoding{#tiffencoding}

TIFF编码格式。 指定TIFF图像的压缩格式（实际上是`fmt=`命令的第三个值的默认值）。

设置为`0`表示无压缩，`1`表示LZW，`2`表示deflate (ZIP)，`3`表示JPEG压缩。

## 属性 {#section-469f5a1225464542866f5353edd92db3}

枚举。

## 默认 {#section-a3c5152a9f464e4987ed7c05d35b1169}

如果未定义或为空，则从`default::TiffEncoding`继承。

## 另请参阅 {#section-1601425e5ac3486da4df8e7fa55981b2}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)

