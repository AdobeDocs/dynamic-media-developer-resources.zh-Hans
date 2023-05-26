---
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备通过图像创作创建的内容，以便通过图像渲染进行部署。
solution: Experience Manager
title: 晕影转换器
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# 晕影转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备通过图像创作创建的内容，以便通过图像渲染进行部署。

[!DNL vntc] 位于[！DNL *[!DNL install_root]*\ImageServing\bin]。 具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔生产晕影(请参阅 [晕影缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 生成生产文件柜和窗口覆盖样式文件(请参阅 `-resolution` 和 `-jpegquality`)。

* 可以生成晕影、文件柜和窗口覆盖样式文件的不同文件版本，以便与旧版本的“图像渲染”一起使用。
* 从全分辨率或缩略图的晕影中提取视图图像(请参阅 `-thumbwidth` 和 `-image`)。
* 从源文件中提取相关属性(请参阅 `-info`)，并将它们发送至 `stdout` 或可选日志文件(请参阅 `-log`)。

当使用 [!DNL vntc] 是可选的，强烈建议使用该选项以获得最佳服务器性能。 [!DNL vntc] 此外，还实施广泛的错误检查，并可防止在勤奋使用时出现的严重服务器问题（包括崩溃）。

生成生成晕影时，将输出晕影的像素宽度（如果是金字塔或多分辨率晕影，则为0）附加到生成的输出晕影文件的名称中。 处理CAB样式文件时，输出分辨率会附加到输出文件名中。 所有输出文件（包括可选的缩略图、图像和日志文件以及生产晕影或CAB样式文件）都放在同一目录中，其中 *[!DNL sourceFile]* 位置(除非 `-destPath` 指定了)。

[!DNL vntc] 默认限制为最多3GB内存。 当Vntc达到此限制时，它将停止处理并将产生错误。 此限制可使用以下方式更改 `-maxmem`.

>[!NOTE]
>
>图像创作中的晕影更新工具也可用于准备用于图像渲染的晕影。 同样，内容创作工具能够生成用于图像渲染的压缩样式文件。 使用 [!DNL vntc] 如果处理过程要自动化。 图像创作中的工具包括图形用户界面，因此通常更易于以交互方式使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
