---
description: 图像渲染支持采用ISO-8859-1和UTF-8编码的材料目录。
solution: Experience Manager
title: 字符编码
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# 字符编码{#character-encoding}

图像渲染支持采用ISO-8859-1和UTF-8编码的材料目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 当在每个材料目录文件的最开头处检测到此字符序列时，假定使用UTF-8编码。 任何其他字节序列都会导致文件被解释为已编码为ISO-8859-1标准。

许多当代应用程序在为UTF-8配置后，会自动插入物料清单。
