---
description: 本主题介绍vntc使用语法。
seo-description: 本主题介绍vntc使用语法。
seo-title: 使用
solution: Experience Manager
title: 使用
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 使用{#usage}

本主题介绍vntc使用语法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要处理的文件的路径和名称。 可以是相对于当前工作目录的路径或绝对路径。 必须是有效的暗角、文件柜样式或覆盖样式文件的窗口，并具有以下后缀之一： [!DNL .vnt]、 [!DNL .vnc]或 [!DNL .vnw]。 必需.

*[!DNL destFile]* 是输出晕影文件的路径和名称。 如果未指定，则输出文件将放置在使用指定的文件夹中 `-destpath`。 在这种情况下，文件名会从输入文件名和大小后缀自动生成，后缀以指定的字符串分隔 `-separator`。 对于暗角，大小后缀是单分辨率输出暗角的像素宽度、多分辨率输出暗角的第一视图的宽度，或金字塔暗角的“0”。 对于文件柜样式文件，输出分辨率用作文件后缀。 *[!DNL destFile]* 在指定时 `-info` 忽略。
