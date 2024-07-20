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

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]`分

默认情况下，`trimMargin`设置为由`viewWidth`和`viewHeight`定义的文档的完整大小。 如果未指定，*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值将默认为&#x200B;*[!DNL top]*&#x200B;值。
