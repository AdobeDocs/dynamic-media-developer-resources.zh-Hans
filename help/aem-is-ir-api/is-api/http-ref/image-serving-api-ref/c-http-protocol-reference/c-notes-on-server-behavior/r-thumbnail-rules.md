---
description: 注意这些缩略图规则。
seo-description: 注意这些缩略图规则。
seo-title: 缩略图规则
solution: Experience Manager
title: 缩略图规则
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d04b923-e062-4764-9e48-99a7bba72d3f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 缩略图规则{#thumbnail-rules}

注意这些缩略图规则。

1. 如 `catalog::ThumbType=Crop`果是，则（裁剪）图像将缩放到尽可能小的大小，同时仍覆盖整个目标矩形。 如 `catalog::ThumbType=Fit`果是，则（裁剪）图像将缩放到最大可能的大小，同时仍将整个图像适合目标矩形。 如 `catalog::ThumbType=Texture`果是，则（裁剪）图像会缩放为与之的比 `catalog::ThumbRes` 率 `catalog::Resolution`。
1. 根据和将缩放的图像与目标矩形 `attribute::ThumbHorizAlign` 对齐 `attribute::ThumbVertAlign`。
1. 将结果裁切到目标矩形。

