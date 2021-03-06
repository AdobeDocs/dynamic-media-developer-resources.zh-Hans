---
description: 图像渲染支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。
solution: Experience Manager
title: 图像渲染色彩管理*
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fa772ab2-8a32-4c1a-9ee3-c1cf4a0b3095
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# 图像渲染色彩管理*{#image-rendering-color-management}

图像渲染支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。

**限制**

目前仅支持CMYK、RGB和灰度级色彩空间。

文件柜样式文件(.vnc)和窗口覆盖样式文件( [!DNL .vnw])不进行颜色管理，并假定存在于工作颜色空间中。

**另请参阅**

[国际色彩联盟](https://www.color.org/index.xalter) , [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) , [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) , `attribute::IccProfile*` , `attribute::IccProfileSrc*`, `attribute::IccRenderIntent` , `attribute::IccBlackPointCompensation` , `attribute::IccDither` , ICC配置文件图

## 默认色彩空间 {#section-8ce27edf42e746febe4654f8f19b9c0c}

每个图像目录（和默认目录）都可以定义一组ICC配置文件。 这些配置文件构成此目录的默认色彩空间 — 每个输入配置文件和一个输出配置文件用于灰度、RGB和CMYK数据( `attribute::IccProfileRgb`, `attribute::IccProfileGray`, `attribute::IccProfileCmyk`, `attribute::IccProfileSrcRgb`, `attribute::IccProfileSrcGray`和 `attribute::IccProfileSrcCmyk`)。

特定图像或其他对象的默认色彩空间基于图像的像素类型从目录默认配置文件中选择。

## 输入色彩空间 {#section-660f661a7e954df4b451e34134195276}

材料图像可嵌入ICC配置文件以定义输入色彩空间。 如果源图像中未嵌入任何配置文件， `attribute::IccProfileSrc*` 使用对应于源图像的像素类型的适用图像目录。 如果未在图像目录中定义此属性， `attribute::IccProfile*` 中，将使用。 如果未定义目录属性，则图像不会进行颜色管理，只应用天真的转换。

## 工作色彩空间 {#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作色彩空间由嵌入到晕影中的ICC颜色配置文件定义。 如果晕影不包含用户档案，则默认RGB输入用户档案( `attribute::IccProfileSrcRgb` 会话目录)用于工作色彩空间。

所有渲染操作都在工作色彩空间中执行。

**重要信息：** 工作颜色空间的ICC配置文件必须支持输入和输出转换。 如果将仅输出配置文件用作工作色彩空间，则IR将无法将材料转换到其中。 如果材料存在于相同的工作色空间中，则仍可以使用这种颜色轮廓。 尝试在其他色彩空间中应用材料将失败。

## 显式颜色值 {#section-31727bf1b23e477ca92572fbbf422d2f}

RGB颜色值，指定 `color=`, `bgc=`, `catalog::BgColor`和 `catalog::Color` 假定存在于当前工作颜色空间中。

## 材料数据文件 {#section-33f7a170a6664c02b8479fb89cc0aea3}

材料图像文件（纹理和十字图像）可以具有RGB、灰度或CMYK像素类型，并可以嵌入颜色配置文件。 如果未嵌入任何颜色配置文件，则默认输入颜色空间与图像相关联（例如，材料目录中与图像像素类型对应的颜色配置文件）。

从嵌套的“图像提供”或“图像呈现”请求获得的材料图像通常包括颜色配置文件。 如果不是，则图像与与像素类型对应的默认输入色彩空间相关联。

如果图像文件的颜色空间与工作颜色空间不同，则使用精确的颜色转换来转换为工作颜色空间。 未嵌入配置文件且未定义默认输入配置文件时，会使用天真类型转换。

其他材料数据文件，如文件柜样式文件( [!DNL .vnc])或窗口覆盖文件( [!DNL .vnw])不会嵌入颜色配置文件，并且始终假定该配置文件位于工作颜色空间中。

## 输出色彩空间 {#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作色彩空间中进行。 如果请求使用 `icc=` 命令，则数据会在编码后返回给客户端之前转换为该色彩空间。 禁用色彩管理时，如果需要转换为灰阶或CMYK，则使用天真的转换。

## 嵌入的颜色配置文件 {#section-5ff733832d38429fbe02b3c1e9bb94a9}

通过指定 `iccEmbed=` 请求。

如果 `icc=` 未指定，则工作色空间的ICC配置文件会被嵌入。 如果禁用了色彩管理，并且未使用指定配置文件，则不会嵌入任何配置文件 `icc=`.

## ICC 配置文件 {#section-afeb76068b5042adb83261638e450140}

服务器使用的所有颜色配置文件都必须符合ICC规范。 ICC配置文件通常具有 [!DNL .icc] 或 [!DNL .icm] 文件后缀和与材料数据文件共同位置。

而输出配置文件可以通过 `icc=` 命令，建议在默认目录或特定材料目录的ICC配置文件映射中注册所有配置文件，并使用快捷方式标识符( `icc::Name`)，而不是文件路径。

必须在材料目录或默认目录的ICC配置文件映射中注册工作配置文件。
