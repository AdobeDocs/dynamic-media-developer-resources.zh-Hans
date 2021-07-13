---
description: RTF字符串中引用的所有字体都必须在默认目录或当前图像目录的字体映射文件中可用，否则会返回错误。
solution: Experience Manager
title: 字体处理
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---

# 字体处理{#font-handling}

RTF字符串中引用的所有字体都必须在默认目录或当前图像目录的字体映射文件中可用，否则会返回错误。

通过注册相应的字体文件，可以获得斜体和粗体文本的最佳质量。 如果不可用，则服务器可以从标准面合成粗体和/或斜体字体。 （请参阅` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`。）

在RTF字符串中明确指定“无”时，使用`attribute::DefaultFont`指定的字体。

图像提供支持TrueType、OpenType、Adobe Type1（仅限Windows）字体。

## Photofont®字体支持 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支持Photofont®字体，但具有以下限制：

* `\cf` 在指定照片字体的文本跨区中被忽略；Photofont字面具有预定义的颜色
* 不支持合成的字体样式；使用`\b`和`\i`需要相应的字体映射条目，否则返回错误

* 不支持垂直文本流
* 不支持具有16位图像的Photofont字体
* 不支持每幅图像具有多个字形的PhotoFont字体
* 除非Photofont字形图像嵌入颜色配置文件，否则应用天真颜色转换；在这种情况下，始终应用相对比色渲染意图和黑点补偿

有关其他信息，请参阅` [www.photofont.com](http://www.photofont.com)`。

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[字体映射引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [属性：:SyntherizationFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [属性：:DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
