---
description: 设置修剪边距。 设置PDF文件中设置的修剪边距。
solution: Experience Manager
title: trimMargin
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc6e31f8-d3be-44d3-8342-a4ef4b3fd61b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# trimMargin{#trimmargin}

设置修剪边距。 设置PDF文件中设置的修剪边距。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 点数

默认情况下， `trimMargin` 设置为由定义的文档的完整大小 `viewWidth` 和 `viewHeight`. 此 *[!DNL left]*， *[!DNL bottom]*、和 *[!DNL right]* 值默认为 *[!DNL top]* 值（如果未指定）。
