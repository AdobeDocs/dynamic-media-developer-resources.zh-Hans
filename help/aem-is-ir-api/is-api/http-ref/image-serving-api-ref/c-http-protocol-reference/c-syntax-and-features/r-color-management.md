---
description: 图像服务支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。
solution: Experience Manager
title: 图像服务色彩管理
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 0c9a489c-36e0-4934-b9c5-33414a9ce0b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1200'
ht-degree: 0%

---

# 图像服务色彩管理{#image-serving-color-management}

图像服务支持基于符合ICC（国际颜色联盟）规范的色彩空间配置文件的色彩空间转换。

## 默认色彩空间 {#section-8cfe60808bce49968091995e4e521dba}

每个图像目录（和默认目录）可以定义一组ICC配置文件，这些配置文件构成此目录的默认色彩空间 — 一个输入配置文件和一个输出配置文件，分别用于灰度、RGB和CMYK数据。 请参阅` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`、` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`、` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`、` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`、` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`和` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`。

## 输入色彩空间 {#section-9f08e2c1b6aa4fe4815be174972c1944}

源图像可以嵌入ICC配置文件以定义输入色彩空间。 如果源图像中未嵌入配置文件，则将使用与源图像的像素类型对应的适用图像目录的`attribute::IccProfileSrc*`。 如果图像目录中未定义此属性，则使用`attribute::IccProfile*`。 如果未定义目录属性，则图像不会进行颜色管理，只会应用天真的转换。

## 输出色彩空间 {#section-b517bca622b64dcfa7defba6035d0716}

使用`icc=`命令定义请求的最终图像结果的颜色空间。 如果未指定`icc=`，则与输出图像的像素类型对应的默认输出颜色空间（来自请求的主目录）将用作输出颜色空间。 如果主目录或默认目录中未定义输出配置文件，并且基层是具有与输出像素类型匹配的嵌入配置文件的图像，则该配置文件将用于输出色彩空间。 否则，输出色彩空间仍未定义 — 在像素类型之间进行转换时，只应用天真色彩转换，而输出图像中不能嵌入任何颜色配置文件。

嵌套/嵌入式图像服务请求的输出颜色空间始终与外部嵌入请求的输出颜色空间相同。

## 纯色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果颜色值包含后缀“S”，则使用`color=`、`bgcolor=`或RTF命令`\iscolortbl`指定的颜色值将与输入颜色空间关联，否则，它们与输出颜色空间关联。 使用`bgc=`或RTF命令`\colortbl`和`\cmykcolortbl`指定的颜色值始终与相应的默认或实际输出颜色空间相关联。

>[!NOTE]
>
>此时，`bgc=`未完全参与色彩管理 — 使用`bgc=`指定时，将忽略“S”后缀，当使用`bgc=`指定的颜色值的像素类型与输出图像的像素类型不同时，将应用天真转换。 否则， `bgc=`与实际输出色彩空间相关联。

## 嵌套和嵌入的请求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套IS请求和嵌入IR请求的输出颜色空间自动设置为最外部请求的输出颜色空间，除非嵌套请求指定具有`icc=`的显式输出颜色空间。 此外，嵌套/嵌入的请求还从最外部请求的主目录中继承默认的输出颜色空间，以确保对纯色值的处理一致。

## 色彩空间转换 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

图像提供通常会尝试在处理过程中延迟颜色转换。 如果图像的所有图层具有相同的图层色彩空间，则在合并和最终缩放后转换到输出色彩空间。 如果涉及多个层色彩空间，则在合并之前将每个层转换为输出色彩空间。

>[!NOTE]
>
>命令`op_brightness=`、`op_colorbalance=`、`op_colorize=`、`op_contrast=`、`op_hue=`和`op_saturation=`是RGB操作。 这些操作仅在图层颜色空间具有RGB像素类型时才保持颜色保真度。 如果除RGB之外，数据会使用天真颜色转换转换为RGB，并且结果的颜色保真度将有限。 此类图层的图层色彩空间应视为不确定。

颜色转换选项随`icc=`提供，或者，如果未指定`icc=`，则与`attribute::IccRenderIntent`、`attribute::IccBlackPointCompensation`和`attribute::IccDither`一起提供。

## 嵌入颜色配置文件 {#section-261ebbae5ce046589a776ca972380052}

输出色彩空间的ICC色彩配置文件（如果可用）可通过指定`iccEmbed=`嵌入到响应图像中。

## 管理ICC配置文件 {#section-eb210e4b44e64e2c8b80ee59216c5555}

服务器使用的所有颜色配置文件都必须符合ICC规范。 ICC配置文件通常具有[!DNL .icc]或[!DNL .icm]文件后缀，并且与图像数据文件共同位置。

虽然输出配置文件可以在`icc=`命令中通过文件路径/名称指定，但建议在默认目录或图像目录的ICC配置文件映射中注册所有配置文件，并使用快捷方式标识符(`icc::Name`)，而不是文件路径。

在`catalog::IccProfile`和`attribute::IccProfile*`中引用的所有ICC配置文件都必须在图像或默认目录的ICC配置文件映射中进行注册。

## 限制 {#section-fb50ede40b124b89b30679da29782ab5}

目前仅支持CMYK、RGB和灰度级色彩空间。

## 包含的ICC颜色配置文件 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

图像提供在默认图像目录中包含大多数标准AdobeICC配置文件。 这些用户档案可通过其通用名称(例如，在Photoshop中可看到)或较短的标识符进行访问。 下表列出了所有标准ICC配置文件。 在`icc=`命令中通过其通用名称引用配置文件时，空格必须编码为`%20`。

其他用户档案可以添加到标准用户档案，添加到默认目录或特定图像目录。 有关详细信息，请参阅[ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)。

>[!NOTE]
>
>下表仅适用于&#x200B;*Dynamic Media Hybrid*（在`dynamicmedia`运行模式下运行）。

|标识符|通用名称|文件名|
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
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间配置文件.icm|
|`WideGamutRGB`|宽色域RGB|WideGayomRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`CoatedGraCol`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|欧洲ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Repande|JapanColor2002Repande.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc|
|`NewsprintSNAP2007`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|未涂层的FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`WebCoatedGrade3`|Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc|
|`WebCoatedGrade5`|Web Coated SWOP 2006五级纸|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

下表适用于&#x200B;*Dynamic Media Classic Image Serving*&#x200B;和&#x200B;*Dynamic Media*（在`dynamicmedia_scene7`运行模式下运行）。

|标识符|通用名称|文件名|
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
|`sRGB`|sRGB IEC61966-2.1|sRgb色彩空间配置文件.icm|
|`WideGamutRGB`|宽色域RGB|WideGayomRGB.icc|
|**CMYK**||
|`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc|
|`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc|
|`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc|
|`EuropeISOCoated`|欧洲ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc|
|`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc|
|`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc|
|`JapanColorCoated`|Japan Color 2001 Coated|JapanColor2001Coated.icc|
|`JapanColorNewspaper`|Japan Color 2002 Repande|JapanColor2002Repande.icc|
|`JapanColorUncoated`|Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc|
|`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc|
|`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc|
|`PS4Default`|Photoshop 4 Default CMYK|Photoshop4DefaultCMYK.icc|
|`PS5Default`|Photoshop 5 Default CMYK|Photoshop5DefaultCMYK.icc|
|`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc|
|`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc|
|`UncoatedFogra29`|未涂层的FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc|
|`US Newsprint (SNAP 2007)`|美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc|
|`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc|
|`WebCoatedFogra28`|Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc|
|`Web Coated SWOP 2006 Grade 3 Paper`|Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc|
|`Web Coated SWOP Grade 5 Paper`|Web Coated SWOP 2006五级纸|WebCoatedSWOP2006Grade5.icc|
|`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

## 另请参阅 {#section-39159397e80b4efca5f631eab8b9aa06}

[国际颜色联盟](http://www.color.org/index.xalter),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [属性：:IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)*,  [属性：:IccProfileSrc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)*,  [属性：:IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [属性：:IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [属性：IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [ICC配置文件映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [, ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)color= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)bgc，  [ *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
