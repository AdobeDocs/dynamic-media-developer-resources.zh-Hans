---
description: 图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。
seo-description: 图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。
seo-title: 字符编码
solution: Experience Manager
title: 字符编码
topic: Scene7 Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 字符编码{#character-encoding}

图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 在每个图像目录文件的最开始处检测到此字符序列时，将采用UTF-8编码。 任何其他字节序列导致文件被解释为已编码到ISO-8859-1标准。

许多当代应用程序在配置为UTF-8时会自动插入BOM。
