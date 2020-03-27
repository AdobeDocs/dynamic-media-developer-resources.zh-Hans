---
description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
seo-description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
seo-title: 字体处理
solution: Experience Manager
title: 字体处理
topic: Scene7 Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 字体处理{#font-handling}

RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。

通过注册相应的字体文件，可以获得斜体和粗体文本的最佳质量。 如果不可用，服务器可以从标准字面合成粗体和／或斜体字体。 （请参阅` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`。）

当RTF字符串中显 `attribute::DefaultFont` 式指定无字体时，将使用指定的字体。

图像服务支持TrueType、OpenType、Adobe Type 1（仅限Windows）字体。

## Photofont®字体支持 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支持Photofont®字体，但有以下限制：

* `\cf` 在指定Photofont字体的文本范围中忽略；Photoshop字体脸部具有预定义的颜色
* 不支持合成的字体样式；使用并 `\b` 需要 `\i`相应的字体映射条目，否则将返回错误

* 不支持垂直文本流
* 不支持具有16位图像的Photofont字体
* 不支持每幅图像具有多种字形的Photofont字体
* 除非Photofont字形图像嵌入颜色用户档案，否则将应用天真的颜色转换；在这种情况下，始终应用相对比色渲染方法和黑点补偿

Refer to ` [www.photofont.com](http://www.photofont.com)` for additional information.

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)，属 [性：:SynthesingFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)，属 [性：:DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](http://www.photofont.com)
