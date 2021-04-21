---
description: 图像服务支持ISO-8859-1和UTF-8编码的图像目录。
solution: Experience Manager
title: 字符编码
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 字符编码{#character-encoding}

图像服务支持ISO-8859-1和UTF-8编码的图像目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 在每个图像目录文件的最开始处检测到此字符序列时，假定采用UTF-8编码。 任何其他字节序列导致文件解释为已编码到ISO-8859-1标准。

许多当代应用程序在配置为UTF-8时会自动插入物料清单。
