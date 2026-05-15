---
description: 图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。
solution: Experience Manager
title: 字符编码
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# 字符编码{#character-encoding}

图像服务支持采用ISO-8859-1和UTF-8编码的图像目录。

字节顺序标记(BOM)用于指定每个文件的编码。 对于UTF-8，BOM为字节序列`EF BB BF`。 在每个图像目录文件的开头检测到此字符序列时，将采用UTF-8编码。 任何其他字节序列都会导致该文件被解释为编码为ISO-8859-1标准。

许多当代应用程序在针对UTF-8进行配置时，会自动插入BOM。
