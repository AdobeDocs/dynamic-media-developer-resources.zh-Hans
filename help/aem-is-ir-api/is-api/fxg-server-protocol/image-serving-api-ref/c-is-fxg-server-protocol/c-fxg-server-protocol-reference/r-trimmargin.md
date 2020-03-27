---
description: 设置修剪边距。 设置在PDF文件中设置的裁切边距。
seo-description: 设置修剪边距。 设置在PDF文件中设置的裁切边距。
seo-title: trimMargin
solution: Experience Manager
title: trimMargin
topic: Scene7 Image Serving - Image Rendering API
uuid: af94f9e8-a32e-439a-817a-a40aa8dc7dd4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# trimMargin{#trimmargin}

设置修剪边距。 设置在PDF文件中设置的裁切边距。

` trimMargin=[ *[!DNL top]*[, *[!DNL left]*= *[!DNL top]*[, *[!DNL bottom]*= *[!DNL top]*[, *[!DNL right]*= *[!DNL left]*]]]]` 点

默认情况下， `trimMargin` 将文档设置为和定义的完全大 `viewWidth` 小 `viewHeight`。 如 *[!DNL left]*&#x200B;果未指 *[!DNL bottom]*&#x200B;定，则 *[!DNL right]* 、和值将默认 *[!DNL top]* 为该值。
