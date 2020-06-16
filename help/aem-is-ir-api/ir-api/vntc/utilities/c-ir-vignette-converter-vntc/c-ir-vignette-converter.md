---
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-title: 暗角转换器
solution: Experience Manager
title: 暗角转换器
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---


# 暗角转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。

[!DNL vntc] 位于[!DNL *[!DNL install_root]*\ImageServing\bin]。 它具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔制作晕影(请参 [阅晕影缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 生成生产文件柜和覆盖样式文件的窗口(请 `-resolution` 参阅 `-jpegquality`和)。

* 可以生成晕影、文件柜和窗口封面样式文件的不同文件版本，以便与旧版图像渲染一起使用。
* 从晕影中提取视图图像（全分辨率或缩略图）(请 `-thumbwidth` 参阅 `-image`和)。
* 从源文件提取相关属性(请参 `-info`阅)，并将其发 `stdout` 送到可选日志文件(请参 `-log`阅)。

尽管使用是可 [!DNL vntc] 选的，但强烈建议使用它以获得最佳服务器性能。 [!DNL vntc] 此外，还实施了大量错误检查，并可以防止严重的服务器问题，包括在被认真使用时发生崩溃。

生成生产晕影时，输出晕影的像素宽度（如果是金字塔或多分辨率晕影，则为0）会附加到生成的输出晕影文件的名称中。 处理文件柜样式文件时，输出分辨率将附加到输出文件名。 所有输出文件（包括可选缩略图、图像和日志文件）以及生产暗角或文件柜样式文件都放在所 *[!DNL sourceFile]* 在的目录 `-destPath` 中（除非指定）。

[!DNL vntc] 默认限制为最多3GB内存。 当Vntc达到此限制时，它将停止处理并产生错误。 此限制可使用更改 `-maxmem`。

>[!NOTE] {class=&quot;-主题／注释&quot;
>
>图像创作中的晕影更新工具还可用于准备晕影以用于图像渲染。 同样，内容创作工具能够生成用于图像渲染的文件柜样式文件。 如果 [!DNL vntc] 要自动处理，请使用。 图像创作中的工具包含一个图形用户界面，因此通常更容易交互使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
