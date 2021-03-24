---
description: 本主题介绍vntc用法语法。
solution: Experience Manager
title: 使用
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# 使用{#usage}

本主题介绍vntc用法语法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要处理的文件的路径和名称。可以是相对于当前工作目录的路径或绝对路径。 必须是有效的晕影、文件柜样式或覆盖样式文件的窗口，并具有以下后缀之一：[!DNL .vnt]、[!DNL .vnc]或[!DNL .vnw]。 必需.

*[!DNL destFile]* 是输出晕影文件的路径和名称。如果未指定，则输出文件将放置在用`-destpath`指定的文件夹中。 在这种情况下，文件名将自动从输入文件名和大小后缀中生成，并用用`-separator`指定的字符串分隔。 对于晕影，大小后缀是单分辨率输出晕影的像素宽度、多分辨率输出晕影的第一个视图的宽度，或金字塔晕影的“0”。 对于文件柜样式文件，输出分辨率用作文件后缀。 *[!DNL destFile]* 指定时 `-info` 忽略。
