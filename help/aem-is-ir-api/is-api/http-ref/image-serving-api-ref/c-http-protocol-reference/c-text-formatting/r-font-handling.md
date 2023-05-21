---
title: 字型處理
description: 在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔中使用，否則會傳回錯誤。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# 字型處理{#font-handling}

在RTF字串中參照的所有字型都必須可在預設目錄或目前影像目錄的字型對應檔中使用，否則會傳回錯誤。

登入對應的字型檔案，即可獲得斜體與粗體文字的最佳品質。 如果不可用，伺服器可以從標準字型合成粗體和/或斜體字型。 (請參閱 [attribute：：SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

指定的字型 `attribute::DefaultFont` 當RTF字串中未明確指定任何專案時使用。

「影像伺服」支援TrueType、OpenType、Adobe Type1 （僅限Windows）字型。

## Photofont®字型支援 {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` 支援Photofont®字型，但有下列限制：

* `\cf` 在指定Photofont字型的文字範圍中會被忽略；Photofont字型面具有預先定義的顏色
* 不支援合成字型樣式；使用 `\b` 和 `\i`需要對應的字型對應專案，否則會傳回錯誤

* 不支援垂直文字排列
* 不支援含16位元影像的Photofont字型
* 不支援每個影像有多個字元的Photofont字型
* 除非套用Photofont Glyph影像內嵌色彩設定檔，否則會套用天真的色彩轉換；在這種情況下，一律會套用相對比色演算色彩比對和黑點補償

請參閱 [www.photofont.com](https://www.photofont.com) 以取得其他資訊。

## 另请参阅 {#section-6cb8a802aa044836bbe449d559093f3a}

[字型地圖參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d)， [attribute：：SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)， [attribute：：DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)， [ [!DNL www.photofont.com] ](https://www.photofont.com)
