---
description: 图像渲染支持采用ISO-8859-1和UTF-8编码的材料目录。
seo-description: 图像渲染支持采用ISO-8859-1和UTF-8编码的材料目录。
seo-title: 字符编码
solution: Experience Manager
title: 字符编码
topic: Dynamic Media Image Serving - Image Rendering API
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# 字符编码{#character-encoding}

图像渲染支持采用ISO-8859-1和UTF-8编码的材料目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 在每个材料目录文件的最开始处检测到此字符序列时，将采用UTF-8编码。 任何其他字节序列导致文件被解释为已编码到ISO-8859-1标准。

许多当代应用程序在配置为UTF-8时，会自动插入BOM。
