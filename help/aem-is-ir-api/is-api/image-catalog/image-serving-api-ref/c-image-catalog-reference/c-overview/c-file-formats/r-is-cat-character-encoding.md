---
description: 图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。
solution: Experience Manager
title: 字符编码
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 字符编码{#character-encoding}

图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 当在每个图像目录文件的最开始处检测到此字符序列时，假定使用UTF-8编码。 任何其他字节序列都会导致文件被解释为已编码为ISO-8859-1标准。

许多当代应用程序在为UTF-8配置后，会自动插入物料清单。
