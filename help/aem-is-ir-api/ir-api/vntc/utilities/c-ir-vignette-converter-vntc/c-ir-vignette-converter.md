---
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备通过“图像创作”创建的内容，以便在“图像渲染”中部署。
solution: Experience Manager
title: 晕影转换器
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---

# 晕影转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备通过“图像创作”创建的内容，以便在“图像渲染”中部署。

[!DNL vntc] 位于[!DNL  *[!DNL install_root]*\ImageServing\bin]中。它具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔生产晕影（请参阅[晕影缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)）。
* 生产包含样式文件的生产机柜和窗口（请参阅`-resolution`和`-jpegquality`）。

* 可以生成晕影、文件柜和窗口覆盖样式文件的不同文件版本，以便与早期版本的“图像渲染”一起使用。
* 从小角像中提取视图图像（全分辨率或缩略图）（请参阅`-thumbwidth`和`-image`）。
* 从源文件中提取相关属性（请参阅`-info`），并将其发送到`stdout`或可选日志文件（请参阅`-log`）。

虽然可选使用[!DNL vntc]，但强烈建议使用以获得最佳服务器性能。 [!DNL vntc] 此外，还实施了广泛的错误检查，并可以防止在勤勉使用时出现严重的服务器问题（包括崩溃）。

在生成生产晕影时，输出晕影的像素宽度（在金字塔或多分辨率晕影的情况下为0）会附加到生成的输出晕影文件的名称中。 处理文件柜样式文件时，输出分辨率会附加到输出文件名。 所有输出文件（包括可选缩略图、图像和日志文件以及生产晕影或机柜样式文件）都放置在&#x200B;*[!DNL sourceFile]*&#x200B;所在的同一目录中（除非指定了`-destPath`）。

[!DNL vntc] 默认情况下，将其自身内存限制为最多3GB。当Vntc达到此限制时，它将停止处理并产生错误。 使用`-maxmem`可以更改此限制。

>[!NOTE]
>
>图像创作中的晕影更新工具还可用于准备晕影以用于图像渲染。 同样，内容创作工具能够生成用于图像渲染的文件柜样式文件。 如果要自动处理，请使用[!DNL vntc]。 图像创作中的工具包含一个图形用户界面，因此通常更便于以交互方式使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
