---
description: Digimarc用户信息。 指定Digimarc嵌入的用户信息。
seo-description: Digimarc用户信息。 指定Digimarc嵌入的用户信息。
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# DigimarcId{#digimarcid}

Digimarc用户信息。 指定Digimarc嵌入的用户信息。

## 属性 {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

五、六个以逗号分隔的整数数。 不再使用第三个和第四个数字：

`creator-id, creator-pin, durability [ , chroma ]`

购买 `creator-id` 服 `creator-pin` 务时，Digimarc会提供该服务。 未使用的值应留空。

`durability` 指定Digimarc水印嵌入强度。 它可能为1、2、3或4，其中1表示最弱，4表示最强的耐用性。

设置 `chroma` 为1可将水印编码为图像的色度数据，设置为0（默认）可将其编码为明亮度。 输出灰度图像时忽略此设置。

## 默认 {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

如果未定义 `default::DigimarcId` 或为空，则从中继承。

## 示例 {#section-8469ae1c27b4461da3d53fbabc32d3c5}

指定耐久性设置为4的测试Digimarc创建者id。

`DigimarcId= 404407,32,,,4`

## 另请参阅 {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
