---
title: 晕影转换器
description: 晕影转换器(vntc)是一个命令行实用程序，用于准备通过图像创作创建的内容以进行图像渲染部署。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# 晕影转换器{#vignette-converter}

晕影转换器(vntc)是一个命令行实用程序，用于准备通过图像创作创建的内容以进行图像渲染部署。

[!DNL vntc] 位于[！DNL *[!DNL install_root]*\ImageServing\bin] 它具有以下功能：

* 将主晕影转换为单分辨率、多分辨率或金字塔生产晕影(请参阅 [晕影缩放](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585))。
* 生成生产文件柜和窗口覆盖样式文件(请参阅 `-resolution` 和 `-jpegquality`)。

* 生成晕影、文件柜和窗口覆盖样式文件的不同文件版本，以用于旧版本的“图像渲染”。
* 从全分辨率或缩略图的晕影中提取视图图像(请参阅 `-thumbwidth` 和 `-image`)。
* 从源文件中提取相关属性(请参阅 `-info`)，并将它们发送至 `stdout` 或可选的日志文件(请参阅 `-log`)。

当使用 [!DNL vntc] 可选，Adobe建议使用它以获得最佳服务器性能。 晕影转换器还可以实现广泛的错误检查，并防止在勤奋使用时出现的严重服务器问题（包括崩溃）。

生成生成生成晕影时，输出晕影的像素宽度（如果为金字塔或多分辨率晕影，则为0）将附加到生成的输出晕影文件的名称中。 在处理CAB样式文件时，输出分辨率会附加到输出文件名中。 所有输出文件（包括可选的缩略图、图像和日志文件以及生产晕影或文件柜样式文件）都放在同一目录中，其中 *[!DNL sourceFile]* 位置(除非 `-destPath` 指定了)。

默认情况下，晕影转换器将自身限制为最多3 GB的内存。 当vntc达到此限制时，它将停止处理并产生错误。 可使用以下方式更改此限制 `-maxmem`.

>[!NOTE]
>
>图像创作中的晕影更新工具也可用于准备晕影以用于图像渲染。 同样，“内容创作工具”可以生成用于“图像渲染”的文件柜样式文件。 使用 [!DNL vntc] 如果处理要自动化。 图像创作中的工具包括图形用户界面，因此通常更易于以交互方式使用。

## 另请参阅 {#section-3c756bf17b634543904fdd928adeafb2}

图像创作文档
