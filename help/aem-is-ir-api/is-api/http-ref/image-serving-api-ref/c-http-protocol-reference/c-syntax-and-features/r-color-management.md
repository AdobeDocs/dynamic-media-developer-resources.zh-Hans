---
description: 图像服务支持基于符合ICC（国际色彩联盟）规范的色彩空间用户档案的色彩空间转换。
solution: Experience Manager
title: 图像服务颜色管理
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '1195'
ht-degree: 0%

---


# 图像服务颜色管理{#image-serving-color-management}

图像服务支持基于符合ICC（国际色彩联盟）规范的色彩空间用户档案的色彩空间转换。

## 默认色彩空间{#section-8cfe60808bce49968091995e4e521dba}

每个图像目录（和默认目录）可以定义一组ICC用户档案，这些用户档案构成此目录的默认色彩空间——每个图像都对应灰度、RGB和CMYK数据，一个输入和一个输出。 请参阅` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`和` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`。

## 输入色彩空间{#section-9f08e2c1b6aa4fe4815be174972c1944}

源图像可嵌入ICC用户档案以定义输入色彩空间。 如果源图像中未嵌入任何用户档案，则将使用与源图像的像素类型对应的适用图像目录的`attribute::IccProfileSrc*`。 如果未在图像目录中定义此属性，则使用`attribute::IccProfile*`。 如果未定义该目录属性，则图像不进行颜色管理，只应用幼稚的转换。

## 输出色彩空间{#section-b517bca622b64dcfa7defba6035d0716}

请求的最终图像结果的色彩空间由`icc=`命令定义。 如果未指定`icc=`，则使用与输出图像的像素类型对应的默认输出色彩空间（来自请求的主目录）作为输出色彩空间。 如果主目录或默认目录中未定义输出用户档案，并且基层是具有与输出像素类型匹配的嵌入用户档案的图像，则该用户档案将用于输出色彩空间。 否则，输出色彩空间仍未定义——在像素类型之间进行转换时，只应用天真的色彩转换，并且输出图像中不能嵌入任何色彩用户档案。

嵌套／嵌入式图像服务请求的输出色彩空间始终与外部嵌入请求的输出色彩空间相同。

## 纯色{#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果颜色值包含后缀“S”，则用`color=`、`bgcolor=`或RTF命令`\iscolortbl`指定的颜色值将与输入色彩空间关联，否则它们与输出色彩空间关联。 使用`bgc=`或RTF命令`\colortbl`和`\cmykcolortbl`指定的颜色值始终与相应的默认或实际输出色彩空间相关联。

>[!NOTE]
>
>此时，`bgc=`未完全参与色彩管理——当用`bgc=`指定时，将忽略“S”后缀；当用`bgc=`指定的颜色值的像素类型与输出图像的像素类型不同时，将应用天真转换。 否则，`bgc=`与实际输出色彩空间相关联。

## 嵌套和嵌入的请求{#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套IS请求和嵌入IR请求的输出色彩空间自动设置为最外层请求的输出色彩空间，除非嵌套请求指定具有`icc=`的显式输出色彩空间。 此外，嵌套／嵌入式请求还从最外层请求的主目录继承默认输出色彩空间，以确保对纯色值的一致处理。

## 色彩空间转换{#section-ca87b80b8e364ea59d8a92d87121b0fb}

图像服务通常尝试在处理过程中延迟颜色转换。 如果图像的所有图层都具有相同的图层色彩空间，则在合并和最终缩放后转换为输出色彩空间。 如果涉及多个图层色彩空间，则在合并之前将每个图层转换为输出色彩空间。

>[!NOTE]
>
>命令`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`和`op_saturation=`是RGB操作。 这些操作仅在图层颜色空间具有RGB像素类型时才保持颜色保真度。 如果除RGB之外，数据使用天真的颜色转换转换为RGB，结果的颜色保真度将有限。 此类图层的图层色彩空间应被视为不确定。

颜色转换选项随`icc=`提供，或者，如果未指定`icc=`，则与`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`和`attribute::IccDither`一起提供。

## 嵌入颜色用户档案{#section-261ebbae5ce046589a776ca972380052}

输出色彩空间的ICC色彩用户档案（如果可用）可通过指定`iccEmbed=`嵌入到响应图像中。

## 管理ICC用户档案{#section-eb210e4b44e64e2c8b80ee59216c5555}

服务器使用的所有颜色用户档案都必须符合ICC规范。 ICC用户档案文件通常具有[!DNL .icc]或[!DNL .icm]文件后缀，并与图像数据文件共同定位。

虽然输出用户档案可以通过`icc=`命令中的文件路径／名称指定，但建议在默认目录或图像目录的ICC用户档案映射中注册所有用户档案文件，并使用快捷方式标识符(`icc::Name`)代替文件路径。

`catalog::IccProfile`和`attribute::IccProfile*`中引用的所有ICC用户档案都必须注册到图像或默认目录的ICC用户档案映射中。

## 限制{#section-fb50ede40b124b89b30679da29782ab5}

此时仅支持CMYK、RGB和灰阶色彩空间。

## 包含ICC颜色用户档案{#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

图像服务在默认图像目录中包含大多数标准AdobeICC用户档案。 这些用户档案可以通过其通用名称(例如，在Photoshop)或稍短的标识符进行访问。 下表列表了所有标准ICC用户档案。 当使用`icc=`命令的公用名称引用用户档案时，空格必须编码为`%20`。

其他用户档案可以添加到标准用户档案，也可以添加到默认目录或特定图像目录。 有关详细信息，请参阅[ICC用户档案映射参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。

>[!NOTE]
>
>下表仅适用于&#x200B;*Dynamic MediaHybrid*（在`dynamicmedia`运行模式下运行）。

|标识符|公用名|文件名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB`|CIE RGB|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto`|ProPhoto RGB|ProPhoto.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间用户档案.icm|
|`WideGamutRGB`|宽色域RGB|WideGaytRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|欧洲ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspater.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop4默认CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5默认CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade 5.icc|
|`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

下表适用于&#x200B;*Dynamic Media经典图像服务*&#x200B;和&#x200B;*Dynamic Media*（在`dynamicmedia_scene7`运行模式下运行）。

|标识符|公用名|文件名|
|— |— |— |
|**RGB**|||
|`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc|
|`AppleRGB`|Apple RGB|AppleRGB.icc|
|`CIERGB|CIE RGB`|CIERGB.icc|
|`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc|
|`NTSC`|NTSC(1953)|NTSC1953.icc|
|`PAL`|PAL/SECAM|PAL_SECAM.icc|
|`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm|
|`SMPTE`|SMPTE-C|SMPTE-C.icc|
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间用户档案.icm|
|`WideGamutRGB`|宽色域RGB|WideGaytRGB.icc|
|**CMYK**|||
|`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|欧洲ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Newspaper|JapanColor2002Newspater.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop4默认CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop5默认CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|Uncoated FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade 5.icc|
|`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

## 另请参阅 {#section-39159397e80b4efca5f631eab8b9aa06}

[国际颜色联盟](http://www.color.org/index.xalter), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Embed=属性：:Profile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)，属性 [*:Icc配置文件](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b) [](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) [](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md) [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),Icc属性：Icc配置文件意图*，属性：Icc属性：IccRinderBlack Consortium属性：Icc Black Src PointCompation补偿，Icc混色属性：,ICC用户档案图，色=，色=，色=,  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
