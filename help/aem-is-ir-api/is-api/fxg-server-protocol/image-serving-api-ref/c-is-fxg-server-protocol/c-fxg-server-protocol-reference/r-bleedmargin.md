---
description: 设置出血边距。 设置PDF文件中设置的出血边距。
solution: Experience Manager
title: 出血边距
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: badb8ca5-52ba-4b44-b53f-fb302626adc4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# 出血边距{#bleedmargin}

设置出血边距。 设置PDF文件中设置的出血边距。

`bleedMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 点数

默认情况下， `bleedMargin` 设置为由定义的文档的完整大小 `viewWidth` 和 `viewHeight`. 此 *[!DNL left]*， *[!DNL bottom]*、和 *[!DNL right]* 值默认为 *[!DNL top]* 值（如果未指定）。
