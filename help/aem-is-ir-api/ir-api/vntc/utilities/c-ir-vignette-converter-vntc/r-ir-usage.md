---
title: 使用
description: 本主题介绍vntc使用语法。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 161
ht-degree: 1%

---

# 使用{#usage}

本主题介绍vntc使用语法。

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]*&#x200B;是要处理的文件的路径和名称。 它可以是相对于当前工作目录的路径或绝对路径。 它必须是有效的晕影、文件柜样式或窗口覆盖样式文件，并具有以下后缀之一：

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

必需.

*[!DNL destFile]*&#x200B;是输出晕影文件的路径和名称。 如果未指定，则输出文件将放在使用`-destpath`指定的文件夹中。 在此方案中，文件名自动从输入文件名和大小后缀生成，以`-separator`指定的字符串分隔。 对于晕影，大小后缀是单分辨率输出晕影的像素宽度、多分辨率输出晕影的第一视图的宽度，或者如果存在金字塔晕影，则为“0”。 对于文件柜样式文件，输出分辨率用作文件后缀。 在指定`-info`时，*[!DNL destFile]*&#x200B;将被忽略。

