---
description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
seo-description: RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。
seo-title: 字体处理
solution: Experience Manager
title: 字体处理
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 字体处理{#font-handling}

RTF字符串中引用的所有字体必须在默认目录或当前图像目录的字体映射文件中可用，否则将返回错误。

通过注册相应的字体文件，可以获得斜体和粗体文本的最佳质量。 如果不可用，服务器可以从标准字面合成粗体和/或斜体字体。 （请参阅` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`。）

如果RTF字符串中未明确指定任何字体，则使用用`attribute::DefaultFont`指定的字体。

图像服务支持TrueType、OpenType、Adobe Type 1（仅限Windows）字体。

## Photofont®字体支持{#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支持Photofont®字体，但有以下限制：

* `\cf` 在指定Photofont字体的文本跨距中忽略；Photofont字面具有预定义的颜色
* 不支持合成字体样式；使用`\b`和`\i`需要相应的字体映射条目，否则返回错误

* 不支持垂直文本流
* 不支持具有16位图像的Photofont字体
* 不支持每幅图像具有多种字形的Photofont字体
* 除非Photofont字形图像嵌入颜色用户档案，否则将应用天真的颜色转换；在这种情况下，始终应用相对比色渲染方法和黑点补偿

有关其他信息，请参阅` [www.photofont.com](http://www.photofont.com)`。

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[Font Map Reference](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [属性：:InsheatingFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)，属 [性：:DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
