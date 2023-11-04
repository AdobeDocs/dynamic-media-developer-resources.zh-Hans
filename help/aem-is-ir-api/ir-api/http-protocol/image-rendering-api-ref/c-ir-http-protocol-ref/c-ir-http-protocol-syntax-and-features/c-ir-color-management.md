---
description: 图像渲染支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。
solution: Experience Manager
title: 图像渲染颜色管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 0%

---

# 图像渲染颜色管理*{#image-rendering-color-management}

图像渲染支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。

**限制**

目前仅支持CMYK、RGB和灰度颜色空间。

CAB样式文件(.vnc)和窗口覆盖样式文件( [!DNL .vnw])不是色彩管理的，并且假定存在于工作色彩空间中。

**另请参阅**

[国际彩色联盟](https://www.color.org/index.xalter) ， [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ， [`iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ， `attribute::IccProfile*` ， `attribute::IccProfileSrc*`， `attribute::IccRenderIntent` ， `attribute::IccBlackPointCompensation` ， `attribute::IccDither` ， ICC配置文件图

## 默认颜色空间 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每个图像目录（和默认目录）可以定义一组ICC配置文件。 这些配置文件构成此目录的默认色彩空间 — 灰度、RGB和CMYK数据各有一个输入和一个输出配置文件( `attribute::IccProfileRgb`， `attribute::IccProfileGray`， `attribute::IccProfileCmyk`， `attribute::IccProfileSrcRgb`， `attribute::IccProfileSrcGray`、和 `attribute::IccProfileSrcCmyk`)。

特定图像或其他对象的默认颜色空间是基于图像的像素类型从目录默认配置文件中选择的。

## 输入颜色空间 {#section-660f661a7e954df4b451e34134195276}

材质图像可以嵌入ICC配置文件以定义输入颜色空间。 如果源映像中未嵌入任何配置文件， `attribute::IccProfileSrc*` 使用对应于源图像的像素类型的适用图像目录中的。 如果未在图像目录中定义此属性， `attribute::IccProfile*` 已使用。 如果目录属性也未定义，则图像不是颜色管理的，仅应用朴素转换。

## 工作色彩空间 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作颜色空间由嵌入到晕影中的ICC颜色配置文件定义。 如果晕影不包含配置文件，则默认RGB输入配置文件( `attribute::IccProfileSrcRgb` （包含会话目录）作为工作色彩空间。

所有渲染操作都在工作色彩空间中执行。

**重要提示：** 工作色彩空间的ICC配置文件必须支持输入和输出转换。 如果仅输出轮廓用作工作色域，则IR无法将材料转换为它。 如果材料存在于相同的工作色空间中，则这种色彩轮廓仍然可以使用。 尝试在其他颜色空间中应用材质失败。

## 显式颜色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

指定的颜色值RGB `color=`， `bgc=`， `catalog::BgColor`、和 `catalog::Color` 被假定存在于当前工作色彩空间中。

## 材质数据文件 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材质图像文件（纹理和贴花图像）可以具有RGB、灰度或CMYK像素类型，并且可以嵌入颜色配置文件。 如果未嵌入颜色配置文件，则默认输入颜色空间与图像相关联（例如，与图像的像素类型对应的材质目录中的颜色配置文件）。

从嵌套图像服务或图像渲染请求获得的材料图像通常包括颜色配置文件。 如果不是这种情况，则图像与对应于像素类型的默认输入色彩空间相关联。

如果图像文件的颜色空间与工作颜色空间不同，则使用精确的颜色转换来转换为工作颜色空间。 当未嵌入配置文件且未定义默认输入配置文件时，使用朴素类型转换。

其他材料数据文件，如文件柜样式文件( [!DNL .vnc])或窗口覆盖文件( [!DNL .vnw])不嵌入颜色配置文件，并始终假定它在工作颜色空间中。

## 输出颜色空间 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作色彩空间中进行。 如果请求使用指定不同的颜色配置文件 `icc=` 命令，将数据转换为该颜色空间，然后对其进行编码并返回给客户端。 禁用颜色管理时，如有必要，会使用朴素转换来转换为灰度或CMYK。

## 嵌入的颜色配置文件 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

通过指定，可以将与呈现的图像相关联的颜色配置文件嵌入到响应图像中 `iccEmbed=` 请求的。

如果 `icc=` 未指定，将嵌入工作色彩空间的ICC配置文件。 如果禁用了颜色管理并且没有使用指定配置文件，则不会嵌入任何配置文件 `icc=`.

## ICC 配置文件 {#section-afeb76068b5042adb83261638e450140}

服务器使用的所有颜色配置文件都必须符合ICC规范。 ICC配置文件通常具有 [!DNL .icc] 或 [!DNL .icm] 文件后缀，并与材料数据文件共存。

虽然输出配置文件可通过中的文件路径/名称指定 `icc=` 命令，建议在缺省目录或特定材质目录的“ICC配置文件映射”中注册所有配置文件并使用快捷标识符( `icc::Name`)而不是文件路径。

工作配置文件必须在材料目录或默认目录的ICC配置文件映射中注册。
