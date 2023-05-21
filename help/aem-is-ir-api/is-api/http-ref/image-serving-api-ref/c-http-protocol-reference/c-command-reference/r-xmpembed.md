---
description: 內嵌XMP中繼資料。 指定是否應在回應影像中包含XMP中繼資料。
solution: Experience Manager
title: xmpEmbed
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

內嵌XMP中繼資料。 指定是否應在回應影像中包含XMP中繼資料。

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP資料會從來源影像傳遞至回應影像，而不會進行修改。 這可能會導致回應影像中嵌入了不正確的資料。

## 屬性 {#section-27024c4272f44d9a8c264a0629193af2}

要求屬性。 如果來源影像不包含XMP資料，則忽略。 僅來自來源影像的XMP資料 `layer=0` 都會被處理。 會忽略其他圖層影像的XMP資料。

如果輸出影像格式不支援XMP內嵌，則忽略。 請參閱 `fmt=` 以取得支援XMP內嵌的輸出影像格式清單。

## 默认 {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`，不會將路徑內嵌在輸出影像中。

## 另请参阅 {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
