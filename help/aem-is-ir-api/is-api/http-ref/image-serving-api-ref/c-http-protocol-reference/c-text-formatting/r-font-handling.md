---
title: 字体处理
description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 字体处理{#font-handling}

RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。

通过注册相应的字体文件，可以获得斜体和粗体文本的最佳质量。 如果不可用，服务器可以从标准字型合成粗体和/或斜体字型。 (请参阅 [attribute：：SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

指定的字体 `attribute::DefaultFont` 在RTF字符串中未明确指定任何内容时使用。

图像服务支持TrueType、OpenType、Adobe Type1（仅限Windows）字体。

## Photofont®字体支持 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支持Photofont®字体，具有以下限制：

* `\cf` 在指定Photofont字体的文本范围内被忽略；Photofont字体具有预定义的颜色
* 不支持合成字体样式；使用 `\b` 和 `\i`需要相应的字体映射条目，否则返回错误

* 不支持垂直文本流
* 不支持具有16位图像的照片字体
* 不支持每幅图像具有多个字形的Photofont字体
* 除非照片字体字形图像嵌入颜色配置文件，否则将应用天真的颜色转换；在这种情况下，始终应用相对比色渲染意图和黑点补偿

请参阅 [www.photofont.com](https://www.photofont.com) 以获取其他信息。

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[字体映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)， [attribute：：SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)， [attribute：：DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)， [ [!DNL www.photofont.com] ](https://www.photofont.com)
