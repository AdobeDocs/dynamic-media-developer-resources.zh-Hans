---
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-description: 晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。
seo-title: 暗角转换器
solution: Experience Manager
title: 暗角转换器
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 暗角转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备使用图像创作创建的内容，以便通过图像渲染进行部署。

[!DNL vntc] 位于[!DNL *[!DNL install_root]*\ImageServing\bin]中。 它具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔制作晕影(请参 [阅暗角缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 生产生产机柜和覆盖样式文件的窗口(请参 `-resolution` 阅和 `-jpegquality`)。

* 可以生成晕影、文件柜和窗口封面样式文件的不同文件版本，以便与旧版本的图像渲染一起使用。
* 从晕影（全分辨率或缩略图）中提取视图图像(请参 `-thumbwidth` 阅和 `-image`)。
* 从源文件中提取相关属性(请参 `-info`阅)，并将其发送到 `stdout` 或可选日志文件(请参阅 `-log`)。

尽管使用是可选的， [!DNL vntc] 但强烈建议使用它以获得最佳服务器性能。 [!DNL vntc] 还实施了大量错误检查，并可以防止在使用时出现严重的服务器问题，包括崩溃。

在生成生产暗角时，输出暗角的像素宽度（如果是金字塔形或多分辨率暗角，则为0）将附加到生成的输出暗角文件的名称中。 处理文件柜样式文件时，输出分辨率将附加到输出文件名。 所有输出文件（包括可选缩略图、图像和日志文件）以及生产暗角或文件柜样式文件都放置在所 *[!DNL sourceFile]* 在的目录中(除非 `-destPath` 指定)。

[!DNL vntc] 默认情况下，将其自身限制为最多3GB内存。 当Vntc达到此限制时，它将停止处理并将产生错误。 此限制可使用更改 `-maxmem`。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>图像创作中的晕影更新工具还可用于准备晕影以用于图像渲染。 同样，内容创作工具能够生成用于图像渲染的文件柜样式文件。 如果 [!DNL vntc] 要自动处理，则使用。 图像创作中的工具包括图形用户界面，因此通常更易于交互使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
