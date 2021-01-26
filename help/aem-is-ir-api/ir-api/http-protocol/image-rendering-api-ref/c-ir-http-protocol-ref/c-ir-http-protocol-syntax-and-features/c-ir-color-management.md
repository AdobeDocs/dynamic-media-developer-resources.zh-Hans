---
description: 图像渲染支持基于符合ICC（国际颜色协会）规范的色彩空间用户档案的色彩空间转换。
seo-description: 图像渲染支持基于符合ICC（国际颜色协会）规范的色彩空间用户档案的色彩空间转换。
seo-title: 图像渲染色彩管理*
solution: Experience Manager
title: 图像渲染色彩管理*
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9c47f584-645f-4eb7-bdc0-fdef459da3b2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---


# 图像渲染色彩管理*{#image-rendering-color-management}

图像渲染支持基于符合ICC（国际颜色协会）规范的色彩空间用户档案的色彩空间转换。

**限制**

此时仅支持CMYK、RGB和灰阶色彩空间。

文件柜样式文件(.vnc)和窗口封面样式文件([!DNL .vnw])不进行颜色管理，假定工作颜色空间中存在。

**另请参阅**

[国际颜色协](http://www.color.org/index.xalter) 会 [ `icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06) ,  [ `iccEmbed=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f) ,  `attribute::IccProfile*` ,  `attribute::IccProfileSrc*`,  `attribute::IccRenderIntent` ,  `attribute::IccBlackPointCompensation`  `attribute::IccDither` ICC用户档案图

## 默认色彩空间{#section-8ce27edf42e746febe4654f8f19b9c0c}

每个图像目录（和默认目录）都可以定义一组ICC用户档案。 这些用户档案构成此目录的默认色彩空间——灰度、RGB和CMYK数据（`attribute::IccProfileRgb`、`attribute::IccProfileGray`、`attribute::IccProfileCmyk`、`attribute::IccProfileSrcRgb`、`attribute::IccProfileSrcGray`和`attribute::IccProfileSrcCmyk`）各一个输入和一个输出用户档案。

特定图像或其他对象的默认色彩空间会根据图像的像素类型从目录默认用户档案中选择。

## 输入色彩空间{#section-660f661a7e954df4b451e34134195276}

材料图像可嵌入ICC用户档案以定义输入色彩空间。 如果源图像中未嵌入任何用户档案，则将使用与源图像的像素类型对应的适用图像目录的`attribute::IccProfileSrc*`。 如果未在图像目录中定义此属性，则使用`attribute::IccProfile*`。 如果未定义该目录属性，则图像不进行颜色管理，只应用幼稚的变换。

## 工作色彩空间{#section-645d9cfa5b0347a190a0ece218f5b5e1}

通常，工作色彩空间由嵌入在暗角中的ICC颜色用户档案定义。 如果暗角不包括用户档案，则使用默认的RGB输入用户档案（会话目录的`attribute::IccProfileSrcRgb`）作为工作色彩空间。

所有渲染操作都在工作色彩空间中执行。

**重要：** 工作颜色空间的ICC用户档案必须支持输入和输出转换。如果将仅输出用户档案用作工作色彩空间，则IR将无法将材料转换为它。 如果同一工作色彩空间中存在材料，仍可使用这种色彩用户档案。 尝试在其他色彩空间中应用材料将失败。

## 显式颜色值{#section-31727bf1b23e477ca92572fbbf422d2f}

使用`color=`、`bgc=`、`catalog::BgColor`和`catalog::Color`指定的RGB颜色值假定存在于当前工作颜色空间中。

## 材料数据文件{#section-33f7a170a6664c02b8479fb89cc0aea3}

材料图像文件（纹理和德卡尔图像）可以具有RGB、灰度或CMYK像素类型，并可嵌入颜色用户档案。 如果未嵌入任何颜色用户档案，则默认输入色彩空间与图像相关联(例如，来自材料目录的颜色用户档案与图像的像素类型相对应)。

从嵌套的图像服务或图像渲染请求获得的材料图像通常包括颜色用户档案。 如果不是，则图像与与像素类型对应的默认输入色彩空间相关联。

如果图像文件的色彩空间与工作色彩空间不同，则使用精确的色彩转换来转换为工作色彩空间。 在未嵌入用户档案且未定义默认输入用户档案时，会使用天真类型转换。

其他材料数据文件(如文件柜样式文件([!DNL .vnc])或窗口覆盖文件([!DNL .vnw]))不嵌入颜色用户档案，并且始终假定在工作颜色空间中。

## 输出色彩空间{#section-4c2c4dfedbb8429ba5cfddc3d3eab6c4}

所有渲染操作都在工作色彩空间中进行。 如果请求使用`icc=`命令指定不同的颜色用户档案，则数据将在编码前转换为该色彩空间并返回给客户端。 禁用颜色管理时，如果需要将转换为灰度或CMYK，则会使用幼稚的转换。

## 嵌入的颜色用户档案{#section-5ff733832d38429fbe02b3c1e9bb94a9}

通过为请求指定`iccEmbed=`，可以将与渲染后的图像关联的颜色用户档案嵌入到响应图像中。

如果未指定`icc=`，则嵌入工作色彩空间的ICC用户档案。 如果禁用颜色管理且未指定`icc=`用户档案，则不嵌入任何用户档案。

## ICC 配置文件 {#section-afeb76068b5042adb83261638e450140}

服务器使用的所有颜色用户档案都必须符合ICC规范。 ICC用户档案文件通常具有[!DNL .icc]或[!DNL .icm]文件后缀，并与材料数据文件共享。

虽然输出用户档案可以通过`icc=`命令中的文件路径／名指定，但建议在默认目录或特定材料目录的ICC用户档案映射中注册所有用户档案文件，并使用快捷方式标识符(`icc::Name`)代替文件路径。

工作用户档案必须在物料目录或默认目录的ICC用户档案图中进行注册。
