---
title: 图像服务颜色管理
description: 图像服务支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '1202'
ht-degree: 0%

---

# 图像服务颜色管理{#image-serving-color-management}

图像服务支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。

## 默认颜色空间 {#section-8cfe60808bce49968091995e4e521dba}

每个图像目录（和默认目录）可以定义一组ICC配置文件，这些配置文件构成此目录的默认RGB空间 — 每个配置文件一个输入和一个输出配置文件用于灰度、颜色和CMYK数据。 参见
[attribute：：IccProfileRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md)
[attribute：：IccProfileGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md)
[属性：：IccProfileCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md)
[attribute：：IccProfileSrcRgb](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md)
[属性：：IccProfileSrcGray](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md)
[属性：：IccProfileSrcCmyk](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md).

## 输入颜色空间 {#section-9f08e2c1b6aa4fe4815be174972c1944}

源图像可以嵌入ICC配置文件以定义输入颜色空间。 如果源图像中未嵌入任何配置文件， `attribute::IccProfileSrc*` 使用对应于源图像的像素类型的适用图像目录中的。 如果未在图像目录中定义此属性， `attribute::IccProfile*` 已使用。 如果目录属性也未定义，则图像不受颜色管理，并且只应用朴素转换。

## 输出颜色空间 {#section-b517bca622b64dcfa7defba6035d0716}

使用定义请求的最终图像结果的颜色空间 `icc=` 命令。 如果 `icc=` 未指定，将与输出图像的像素类型对应的默认输出颜色空间（来自请求的主目录）用作输出颜色空间。 如果在主目录或默认目录中未定义输出配置文件，并且基本图层是具有与输出像素类型匹配的嵌入配置文件的图像，则该配置文件将用于输出颜色空间。 否则，输出色彩空间将保持未定义 — 在像素类型之间进行转换时，仅应用朴素的颜色转换，并且输出图像中无法嵌入任何颜色配置文件。

嵌套/嵌入的图像服务请求的输出颜色空间始终与嵌入的外部请求的输出颜色空间相同。

## 纯色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

指定的颜色值 `color=`， `bgcolor=`或RTF命令 `\iscolortbl` 如果颜色值包括后缀“S”，则它们与输入颜色空间相关联，否则它们与输出颜色空间相关联。 指定的颜色值 `bgc=` 或RTF命令 `\colortbl` 和 `\cmykcolortbl` 始终与相应的默认或实际输出颜色空间相关联。

>[!NOTE]
>
>此时， `bgc=` 未完全参与颜色管理 — 使用指定时，将忽略“S”后缀 `bgc=`，并且当指定的颜色值的像素类型为时，将应用朴素转换 `bgc=` 与输出图像的像素类型不同。 否则， `bgc=` 与实际输出色彩空间相关联。

## 嵌套和嵌入的请求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

除非嵌套请求指定了显式输出颜色空间，否则嵌套的IS请求和嵌入的IR请求的输出颜色空间将自动设置为最外部请求的输出颜色空间 `icc=`. 此外，嵌套/嵌入请求还会从最外层请求的主目录中继承默认输出颜色空间，以确保对纯色值的一致处理。

## 色彩空间转换 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

图像服务通常会在处理期间尝试延迟颜色转换。 如果图像的所有图层都具有相同的图层颜色空间，则在合并和最终缩放之后将转换为输出颜色空间。 如果涉及多个图层色彩空间，则在合并之前将每个图层转换为输出色彩空间。

>[!NOTE]
>
>命令 `op_brightness=`， `op_colorbalance=`， `op_colorize=`， `op_contrast=`， `op_hue=`、和 `op_saturation=` 是RGB操作。 仅当图层颜色空间具有RGB的像素类型时，这些操作才会保持颜色保真度。 如果除了RGB之外，数据还使用朴素的RGB转换转换为颜色，结果将具有有限的色彩保真度。 此类图层的图层颜色空间应视为不确定。

颜色转换选项随 `icc=` 或，如果 `icc=` 未指定，使用 `attribute::IccRenderIntent`， `attribute::IccBlackPointCompensation`、和 `attribute::IccDither`.

## 嵌入颜色配置文件 {#section-261ebbae5ce046589a776ca972380052}

可以通过指定将输出颜色空间的ICC颜色配置文件（如果可用）嵌入响应图像 `iccEmbed=`.

## 管理ICC配置文件 {#section-eb210e4b44e64e2c8b80ee59216c5555}

服务器使用的所有颜色配置文件都必须符合ICC规范。 ICC配置文件通常具有 [!DNL .icc] 或 [!DNL .icm] 文件后缀，并与图像数据文件共存。

虽然输出配置文件可由中的文件路径/名称指定 `icc=` 命令，建议在默认目录或图像目录的ICC配置文件映射中注册所有配置文件并使用快捷方式标识符( `icc::Name`)而不是文件路径。

中引用的所有ICC配置文件 `catalog::IccProfile` 和 `attribute::IccProfile*` 必须在图像或默认目录的ICC配置文件映射中注册。

## 限制 {#section-fb50ede40b124b89b30679da29782ab5}

目前仅支持CMYK、RGB和灰度颜色空间。

## 包含的ICC颜色配置文件 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

图像服务包括默认图像目录中的大多数标准AdobeICC配置文件。 这些配置文件可以通过其通用名称(例如，如Photoshop中所见)或使用较短的标识符进行访问。 下表列出了所有标准ICC配置文件。 在引用配置文件时 `icc=` 命令，空格必须编码为 `%20`.

可以将其他配置文件添加到标准配置文件，也可以添加到默认目录或特定图像目录。 请参阅 [ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 了解详细信息。

>[!NOTE]
>
>下表适用于 *Dynamic Media混合* 仅限(在中运行 `dynamicmedia` 运行模式)。

|标识符|公用名|文件名| |— |— |— | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|AppleRGB|AppleRGB.icc| |`CIERGB`|CIERGB|CIERGB.icc| |`ColorMatchRGB`|ColorMatchRGB|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto`|ProPhotoRGB|ProPhoto.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间Profile.icm| |`WideGamutRGB`|宽色域RGB|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|涂层的FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|涂层的FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`CoatedGraCol`|涂层的GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|欧洲ISO包层FOGRA27|EuropeISOCoatedFOGRA27.icc| |`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001 Coated.icc| |`JapanColorNewspaper`|日本彩色2002报纸|JapanColor2002报纸.icc| |`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001 Uncoated.icc| |`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003 WebCoated.icc| |`JapanWebCoated`|日本Web Coated (Ad)|JapanWebCoated.icc| |`NewsprintSNAP2007`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc| |`PS4Default`|Photoshop 4默认CMYK|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop 5默认CMYK|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc| |`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc| |`UncoatedFogra29`|无涂层的FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc| |`WebCoated`|美国Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|网页涂层的FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`WebCoatedGrade3`|Web涂层的SWOP 2006 3级纸张|WebCoatedSWOP2006Grade3.icc| |`WebCoatedGrade5`|网页包裹SWOP 2006年5级纸张|网页包裹SWOP2006年5级.icc| |`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

下表适用于 *Dynamic Media Classic图像服务* 和 *Dynamic Media* (运行位置 `dynamicmedia_scene7` 运行模式)。

|标识符|公用名|文件名| |— |— |— | |**RGB**||| |`AdobeRGB`|Adobe RGB (1998)|AdobeRGB1998.icc| |`AppleRGB`|AppleRGB|AppleRGB.icc| |`CIERGB|CIE RGB`|CIERGB.icc| |`ColorMatchRGB`|ColorMatchRGB|ColorMatchRGB.icc| |`NTSC`|NTSC (1953)|NTSC1953.icc| |`PAL`|PAL/SECAM|PAL_SECAM.icc| |`ProPhoto RGB`|ProPhotoRGB|ProPhotoRGB.icm| |`SMPTE`|SMPTE-C|SMPTE-C.icc| |`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间Profile.icm| |`WideGamutRGB`|宽色域RGB|WideGamutRGB.icc| |**CMYK**||| |`CoatedFogra27`|涂层的FOGRA27 (ISO 12647-2:2004)|CoatedFOGRA27.icc| |`CoatedFogra39`|涂层的FOGRA39 (ISO 12647-2:2004)|CoatedFOGRA39.icc| |`Coated GRACoL 2006 (ISO 12647-2:2004)`|涂层的GRACoL 2006 (ISO 12647-2:2004)|CoatedGRACoL2006.icc| |`EuropeISOCoated`|欧洲ISO包层FOGRA27|EuropeISOCoatedFOGRA27.icc| |`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc| |`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc| |`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001 Coated.icc| |`JapanColorNewspaper`|日本彩色2002报纸|JapanColor2002报纸.icc| |`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001 Uncoated.icc| |`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003 WebCoated.icc| |`JapanWebCoated`|日本Web Coated (Ad)|JapanWebCoated.icc| |`PS4Default`|Photoshop 4默认CMYK|Photoshop4DefaultCMYK.icc| |`PS5Default`|Photoshop 5默认CMYK|Photoshop5DefaultCMYK.icc| |`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc| |`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc| |`UncoatedFogra29`|无涂层的FOGRA29 (ISO 12647-2:2004)|UncoatedFOGRA29.icc| |`US Newsprint (SNAP 2007)`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc| |`WebCoated`|美国Web Coated (SWOP) v2|USWebCoatedSWOP.icc| |`WebCoatedFogra28`|网页涂层的FOGRA28 (ISO 12647-2:2004)|WebCoatedFOGRA28.icc| |`Web Coated SWOP 2006 Grade 3 Paper`|Web涂层的SWOP 2006 3级纸张|WebCoatedSWOP2006Grade3.icc| |`Web Coated SWOP Grade 5 Paper`|网页包裹SWOP 2006年5级纸张|网页包裹SWOP2006年5级.icc| |`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

## 另请参阅 {#section-39159397e80b4efca5f631eab8b9aa06}

[国际彩色联盟](https://www.color.org/index.xalter)， [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)， [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)， [attribute：：IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)&#42;， [attribute：：IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)&#42;， [attribute：：IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)， [属性：：IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)， [attribute：：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)， [ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)， [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)， [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)， [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
