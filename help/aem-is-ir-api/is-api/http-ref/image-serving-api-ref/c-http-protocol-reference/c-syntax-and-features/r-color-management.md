---
description: 图像服务支持基于符合ICC（国际色彩协会）规范的色彩空间用户档案的色彩空间转换。
seo-description: 图像服务支持基于符合ICC（国际色彩协会）规范的色彩空间用户档案的色彩空间转换。
seo-title: 图像服务颜色管理
solution: Experience Manager
title: 图像服务颜色管理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6291372e-ec4c-4fbd-bffc-b55b1bf2f8cf
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# 图像服务颜色管理{#image-serving-color-management}

图像服务支持基于符合ICC（国际色彩协会）规范的色彩空间用户档案的色彩空间转换。

## 默认色彩空间 {#section-8cfe60808bce49968091995e4e521dba}

每个图像目录（和默认目录）可以定义一组ICC用户档案，它们构成此目录的默认色彩空间——每个输入用户档案和一个输出区域分别用于灰度、RGB和CMYK数据。 See ` [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df)`, ` [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35)`, ` [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)`, ` [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2)`, ` [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)`, and ` [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728)`.

## 输入色彩空间 {#section-9f08e2c1b6aa4fe4815be174972c1944}

源图像可嵌入ICC用户档案以定义输入色彩空间。 如果源图像中没有嵌入用户档案, `attribute::IccProfileSrc*` 将使用与源图像的像素类型相对应的适用图像目录。 如果未在图像目录中定义此属性，则 `attribute::IccProfile*` 使用此属性。 如果未定义该目录属性，则图像不进行颜色管理，只会应用天真的变换。

## 输出色彩空间 {#section-b517bca622b64dcfa7defba6035d0716}

使用命令定义请求的最终图像结果的色彩空 `icc=` 间。 如果 `icc=` 未指定，则使用与输出图像的像素类型相对应的默认输出色彩空间（来自请求的主目录）作为输出色彩空间。 如果主目录或默认目录中未定义输出用户档案，并且基层是具有与输出像素类型匹配的嵌入用户档案的图像，则该用户档案将用于输出色彩空间。 否则，输出色彩空间仍未定义——在像素类型之间转换时只应用天真的颜色转换，并且输出图像中不能嵌入任何颜色用户档案。

嵌套／嵌入式图像服务请求的输出色彩空间始终与外部嵌入请求的输出色彩空间相同。

## 纯色 {#section-df03a5c5ca894e6f8b9a5ba02cf6ac03}

如果颜色值包 `color=`括后缀“S”，则使用、 `bgcolor=``\iscolortbl` 或RTF命令指定的颜色值将与输入色彩空间相关联，否则，它们将与输出色彩空间相关联。 使用或RTF命令 `bgc=` 指定的颜色值， `\colortbl` 始 `\cmykcolortbl` 终与相应的默认或实际输出色彩空间相关联。

>[!NOTE]
>
>此时，不 `bgc=` 完全参与色彩管理——当指定时忽略“S”后缀，并且当指定的颜色值的像素类型与输出图像的像素类型不同时，应用天真的 `bgc=``bgc=` 转换。 否则， `bgc=` 与实际输出色彩空间相关联。

## 嵌套和嵌入的请求 {#section-bdda638c31504f26a77e51ebb1ea6e3b}

嵌套IS请求和嵌入的IR请求的输出色彩空间自动设置为最外层请求的输出色彩空间，除非嵌套请求指定具有显式输出色彩空间 `icc=`。 此外，嵌套／嵌入式请求还从最外层请求的主目录中继承默认的输出色彩空间，以确保对纯色值的一致处理。

## 色彩空间转换 {#section-ca87b80b8e364ea59d8a92d87121b0fb}

图像服务通常尝试在处理过程中延迟颜色转换。 如果图像的所有图层都具有相同的图层色彩空间，则在合并和最终缩放后将转换为输出色彩空间。 如果涉及多个图层色彩空间，则在合并之前将每个图层转换为输出色彩空间。

>[!NOTE]
>
>命令、 `op_brightness=`、、 `op_colorbalance=`和 `op_colorize=`是 `op_contrast=``op_hue=``op_saturation=` RGB操作。 这些操作仅在图层色彩空间具有RGB像素类型时保持颜色保真度。 如果除RGB之外，数据使用天真的颜色转换转换为RGB，并且结果的颜色保真度有限。 此类图层的图层色彩空间应被视为不确定。

颜色转换选项随附 `icc=` 或(如果未指 `icc=` 定)提供， `attribute::IccRenderIntent`与、 `attribute::IccBlackPointCompensation`和一起 `attribute::IccDither`。

## 嵌入颜色用户档案 {#section-261ebbae5ce046589a776ca972380052}

输出色彩空间的ICC色彩用户档案（如果可用）可以通过指定嵌入到响应图像中 `iccEmbed=`。

## 管理ICC用户档案 {#section-eb210e4b44e64e2c8b80ee59216c5555}

服务器使用的所有颜色用户档案必须符合ICC规范。 ICC用户档案文件通常具有 [!DNL .icc] 或文 [!DNL .icm] 件后缀，并与图像数据文件同位。

虽然输出用户档案可以通过命令中的文件路径／名称来指定，但建议在默认目录或图像目录的ICC用户档案图中注册所有用户档案文件，并使用快捷键标识符( `icc=``icc::Name`)代替文件路径。

在中和中引用的所 `catalog::IccProfile` 有ICC用户档案 `attribute::IccProfile*` 必须在图像或默认目录的ICC用户档案映射中进行注册。

## Restrictions {#section-fb50ede40b124b89b30679da29782ab5}

目前仅支持CMYK、RGB和灰度色彩空间。

## 包含ICC颜色用户档案 {#section-98b4a7d9f9814e8ba27d6dcf3dcf850c}

图像服务包括默认图像目录中的大多数标准Adobe ICC用户档案。 这些用户档案可通过其通用名称（例如，Photoshop中所示）或稍短的标识符进行访问。 下表列表了所有标准ICC用户档案。 在命令中按其公用名 `icc=` 引用用户档案时，空格必须编码为 `%20`。

其他用户档案可添加到标准用户档案，即默认目录或特定图像目录。 有关详细信息， [请参阅ICC用户档案图参考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c) 。

>[!NOTE]
>
>下表仅适用于 *Dynamic Media Hybrid* (在运行模 `dynamicmedia` 式下运行)。

|标识符|公用名称|文件名||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB`|CIE RGB|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC(1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto`|ProPhoto RGB|ProPhoto.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`sRGB IEC61966-2.1|sRgb色彩空间用户档案.icm||`WideGamutRGB`|宽色域RGB|WideGalithRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc||`CoatedGraCol`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`EuroscaleCoated`|Euroscale Coated|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`JapanColorWebCoated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc||`NewsprintSNAP2007`美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc||`PS4Default`|Photoshop 4默认CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5默认CMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc||`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`WebCoatedGrade3`Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc||`WebCoatedGrade5`Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade 5.icc||`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

下表适用于 *Dynamic Media Classic(Scene7)图像服务和* Dynamic Media *(在运行*`dynamicmedia_scene7` 模式下运行)。

|标识符|公用名称|文件名||—|—|—||**RGB**|||`AdobeRGB`|Adobe RGB(1998)|AdobeRGB1998.icc||`AppleRGB`|Apple RGB|AppleRGB.icc||`CIERGB|CIE RGB`|CIERGB.icc||`ColorMatchRGB`|ColorMatch RGB|ColorMatchRGB.icc||`NTSC`|NTSC(1953)|NTSC1953.icc||`PAL`|PAL/SECAM|PAL_SECAM.icc||`ProPhoto RGB`|ProPhoto RGB|ProPhoto RGB.icm||`SMPTE`|SMPTE-C|SMPTE-C.icc||`sRGB`sRGB IEC61966-2.1|sRgb色彩空间用户档案.icm||`WideGamutRGB`|宽色域RGB|WideGalithRGB.icc||**CMYK**|||`CoatedFogra27`|Coated FOGRA27(ISO 12647-2:2004)|CoatedFOGRA27.icc||`CoatedFogra39`|Coated FOGRA39(ISO 12647-2:2004)|CoatedFOGRA39.icc||`Coated GRACoL 2006 (ISO 12647-2:2004)`|Coated GRACoL 2006(ISO 12647-2:2004)|CoatedGRACoL2006.icc||`EuropeISOCoated`|Europe ISO Coated FOGRA27|EuropeISOCoatedFOGRA27.icc||`Euroscale Coated v2`|Euroscale Coated v2|EuroscaleCoated.icc||`EuroscaleUncoated`|Euroscale Uncoated v2|EuroscaleUncoated.icc||`JapanColorCoated`Japan Color 2001 Coated|JapanColor2001Coated.icc||`JapanColorNewspaper`Japan Color 2002 Newspaper|JapanColor2002Newspaper.icc||`JapanColorUncoated`Japan Color 2001 Uncoated|JapanColor2001Uncoated.icc||`Japan Color 2003 Web Coated`|Japan Color 2003 Web Coated|JapanColor2003WebCoated.icc||`JapanWebCoated`|Japan Web Coated(Ad)|JapanWebCoated.icc||`PS4Default`|Photoshop 4默认CMYK|Photoshop4DefaultCMYK.icc||`PS5Default`|Photoshop 5默认CMYK|Photoshop5DefaultCMYK.icc||`SheetfedCoated`|美国Sheetfed Coated v2|USSheetfedCoated.icc||`SheetfedUncoated`|美国Sheetfed Uncoated v2|USSheetfedUncoated.icc||`UncoatedFogra29`|Uncoated FOGRA29(ISO 12647-2:2004)|UncoatedFOGRA29.icc||`US Newsprint (SNAP 2007)`美国新闻纸(SNAP 2007)|USNewsprintSNAP2007.icc||`WebCoated`|美国Web Coated(SWOP)v2|USWebCoatedSWOP.icc||`WebCoatedFogra28`Web Coated FOGRA28(ISO 12647-2:2004)|WebCoatedFOGRA28.icc||`Web Coated SWOP 2006 Grade 3 Paper`Web Coated SWOP 2006 3级纸|WebCoatedSWOP2006Grade3.icc||`Web Coated SWOP Grade 5 Paper`Web Coated SWOP 2006 Grade 5 Paper|WebCoatedSWOP2006Grade 5.icc||`WebUncoated`|美国Web Uncoated v2|USWebUncoated.icc|

## 另请参阅 {#section-39159397e80b4efca5f631eab8b9aa06}

[国际颜色联合集团](http://www.color.org/index.xalter), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [Embed=属性：：配置文件](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [icc属性](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)[ *属性：配置文件意图：icc属性*,Icc属性：Icc属性渲染属性：Icc黑色补偿点，黑色补偿点，ICC补偿属性：Icc混色ICC用户档案图，参考色=ICC，色=GC。 *`color`*](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
