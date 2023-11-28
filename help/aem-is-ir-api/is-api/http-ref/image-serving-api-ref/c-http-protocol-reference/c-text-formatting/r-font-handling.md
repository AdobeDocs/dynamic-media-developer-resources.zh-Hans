---
title: 字体处理
description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---

# 字体处理{#font-handling}

RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。

通过注册相应的字体文件，可以获得斜体和粗体文本的最佳质量。 如果不可用，服务器可以从标准字面合成粗体和/或斜体字面。 (请参阅 [attribute：：SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

指定的字体 `attribute::DefaultFont` 在RTF字符串中未明确指定任何内容时使用。

图像服务支持TrueType、OpenType®、Adobe Type1（仅限Windows）字体。

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[字体映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)， [attribute：：SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)， [attribute：：DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
