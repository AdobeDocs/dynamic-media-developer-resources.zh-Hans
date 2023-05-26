---
description: 本主题介绍vntc用法语法。
solution: Experience Manager
title: 使用
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 1%

---

# 使用{#usage}

本主题介绍vntc用法语法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* 是要处理的文件的路径和名称。 可以是相对于当前工作目录的路径或绝对路径。 必须是有效的晕影、文件柜样式或窗口覆盖样式文件，并具有以下后缀之一： [!DNL .vnt]， [!DNL .vnc]，或 [!DNL .vnw]. 必需.

*[!DNL destFile]* 是输出晕影文件的路径和名称。 如果未指定，则输出文件将放置在指定的文件夹中 `-destpath`. 在此方案中，文件名自动从输入文件名和大小后缀生成，用指定的字符串分隔 `-separator`. 对于晕影，大小后缀是单分辨率输出晕影的像素宽度、多分辨率输出晕影的第一视图的宽度，或者在金字塔晕影的情况下为“0”。 对于文件柜样式文件，输出分辨率用作文件后缀。 *[!DNL destFile]* 在以下情况下被忽略 `-info` 已指定。
