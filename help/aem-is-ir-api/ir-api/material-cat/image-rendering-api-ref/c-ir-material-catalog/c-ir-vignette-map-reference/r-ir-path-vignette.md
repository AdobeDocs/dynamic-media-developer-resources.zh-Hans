---
description: 晕影文件路径。 晕影文件的相对路径和名称。
solution: Experience Manager
title: 路径
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5562b0e0-0476-4dd0-acce-058601b9af0a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 10%

---

# 路径{#path}

晕影文件路径。 晕影文件的相对路径和名称。

服务器将此值与`attribute::RootPath`组合，以构建实际的晕影文件路径。 也可以是绝对路径。

## 属性 {#section-b3b295feac084b56bd8a153c04987153}

文本字符串。 可选。如果指定，则必须是有效的相对或绝对文件路径。 如果为空，则`vignette::Modifier`必须包含`vignette=`命令。

## 默认 {#section-a1d2133856084eb79a5be8230a4b38fd}

无。

## 另请参阅 {#section-177131dad5804964bfb8957c1f6e5191}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
