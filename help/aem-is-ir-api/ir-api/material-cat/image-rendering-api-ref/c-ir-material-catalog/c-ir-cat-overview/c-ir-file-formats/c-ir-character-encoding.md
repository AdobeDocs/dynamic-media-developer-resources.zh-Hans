---
description: 图像渲染支持ISO-8859-1和UTF-8编码的材料目录。
seo-description: 图像渲染支持ISO-8859-1和UTF-8编码的材料目录。
seo-title: 字符编码
solution: Experience Manager
title: 字符编码
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# 字符编码{#character-encoding}

图像渲染支持ISO-8859-1和UTF-8编码的材料目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8,BOM是字节序列`EF BB BF`。 在每个材料目录文件的开头检测到此字符序列时，假定采用UTF-8编码。 任何其他字节序列导致文件解释为已编码到ISO-8859-1标准。

许多当代应用程序在配置为UTF-8时，会自动插入物料清单。
