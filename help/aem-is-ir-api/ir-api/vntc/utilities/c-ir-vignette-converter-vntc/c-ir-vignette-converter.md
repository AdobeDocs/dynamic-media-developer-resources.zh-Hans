---
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-title: 晕影转换器
solution: Experience Manager
title: 晕影转换器
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---


# 晕影转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。

[!DNL vntc] 位于[!DNL  *[!DNL install_root]*\ImageServing\bin]。它具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔生产晕影（请参阅[晕影缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)）。
* 生成包含样式文件的生产机柜和窗口（请参阅`-resolution`和`-jpegquality`）。

* 可以生成晕影、文件柜和窗口封面样式文件的不同文件版本，以便与旧版本的图像渲染一起使用。
* 从晕影（全分辨率或缩览图）中提取视图图像（请参阅`-thumbwidth`和`-image`）。
* 从源文件中提取相关属性（请参阅`-info`），并将其发送到`stdout`或可选日志文件（请参阅`-log`）。

尽管使用[!DNL vntc]是可选的，但强烈建议使用以获得最佳服务器性能。 [!DNL vntc] 此外，还实施了广泛的错误检查，并可防止在勤用时出现严重的服务器问题，包括崩溃。

在生成生产晕影时，输出晕影的像素宽度（如果是金字塔或多分辨率晕影，则为0）将附加到生成的输出晕影文件的名称中。 处理文件柜样式文件时，输出分辨率将附加到输出文件名。 所有输出文件（包括可选缩略图、图像和日志文件）以及生产晕影或文件柜样式文件都放置在&#x200B;*[!DNL sourceFile]*&#x200B;所在的同一目录中（除非指定`-destPath`）。

[!DNL vntc] 默认限制为最多3GB内存。当Vntc达到此限制时，它将停止处理并会生成错误。 可以使用`-maxmem`更改此限制。

>[!NOTE]
>
>图像创作中的晕影更新工具还可用于准备晕影以用于图像渲染。 同样，内容创作工具能够生成用于图像渲染的文件柜样式文件。 如果要自动处理，请使用[!DNL vntc]。 图像创作中的工具包含一个图形用户界面，因此通常更容易交互使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
