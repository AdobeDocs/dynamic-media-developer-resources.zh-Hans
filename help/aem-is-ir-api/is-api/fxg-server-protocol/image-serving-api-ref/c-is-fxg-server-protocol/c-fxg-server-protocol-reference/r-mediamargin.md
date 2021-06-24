---
description: 设置媒体边距。 设置在PDF文件中设置的媒体边距。
solution: Experience Manager
title: mediaMargin
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 5bba0dc2-a496-4380-9def-12f9e683eafb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 0%

---

# mediaMargin{#mediamargin}

设置媒体边距。 设置在PDF文件中设置的媒体边距。

` mediaMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 点

默认情况下，`mediaMargin`设置为`viewWidth`和`viewHeight`定义的文档的完整大小。 如果未指定&#x200B;*[!DNL left]*、*[!DNL bottom]*&#x200B;和&#x200B;*[!DNL right]*&#x200B;值，则默认为&#x200B;*[!DNL top]*&#x200B;值。
