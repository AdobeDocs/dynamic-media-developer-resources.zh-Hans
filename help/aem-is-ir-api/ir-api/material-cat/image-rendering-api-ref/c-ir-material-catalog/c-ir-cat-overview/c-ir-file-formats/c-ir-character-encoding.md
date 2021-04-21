---
description: 图像渲染支持ISO-8859-1和UTF-8编码的材料目录。
solution: Experience Manager
title: 字符编码
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# 字符编码{#character-encoding}

图像渲染支持ISO-8859-1和UTF-8编码的材料目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 在每个材料目录文件的开头检测到此字符序列时，假定采用UTF-8编码。 任何其他字节序列导致文件解释为已编码到ISO-8859-1标准。

许多当代应用程序在配置为UTF-8时，会自动插入物料清单。
