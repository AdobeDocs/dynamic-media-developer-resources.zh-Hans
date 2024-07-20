---
description: Digimarc用户信息。 指定Digimarc嵌入的用户信息。
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 3%

---

# DigimarcId{#digimarcid}

Digimarc用户信息。 指定Digimarc嵌入的用户信息。

## 属性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

五或六个逗号分隔的整数。 第三和第四个数字已不再使用：

`creator-id, creator-pin, durability [ , chroma ]`

购买服务时，Digimarc会提供`creator-id`和`creator-pin`。 未使用的值应留空。

`durability`指定Digimarc水印嵌入强度。 它可为1、2、3或4，其中1表示最弱，4表示最强的耐久性。

将`chroma`设置为1可将水印编码到图像的色度数据中，或设置为0（默认值）将其编码到亮度中。 在输出灰度图像时，此设置将被忽略。

## 默认 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

如果未定义或为空，则从`default::DigimarcId`继承。

## 示例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性设置为4的测试Digimarc创建者ID。

`DigimarcId= 404407,32,,,4`

## 另请参阅 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog：：DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
