---
title: 字符编码
description: 图像渲染支持采用ISO-8859-1和UTF-8编码的材质目录。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# 字符编码{#character-encoding}

图像渲染支持采用ISO-8859-1和UTF-8编码的材质目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8，BOM为字节序列`EF BB BF`。 在每个材质目录文件的开头检测到此字符序列时，会采用UTF-8编码。 任何其他字节序列都会导致文件被解释为编码为ISO-8859-1标准。

许多当代应用程序在针对UTF-8进行配置时，会自动插入BOM。
