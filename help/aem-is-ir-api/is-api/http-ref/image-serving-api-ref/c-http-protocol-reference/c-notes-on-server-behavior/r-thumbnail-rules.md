---
description: 请注意这些缩略图规则。
solution: Experience Manager
title: 缩略图规则
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# 缩略图规则{#thumbnail-rules}

请注意这些缩略图规则。

1. 如果为`catalog::ThumbType=Crop`，则（裁剪的）图像将缩放到可能的最小尺寸，同时仍覆盖整个目标矩形。 如果为`catalog::ThumbType=Fit`，则在将整个图像拟合到目标矩形的同时将（裁切）图像缩放到最大尺寸。 如果`catalog::ThumbType=Texture`，（裁剪的）图像将缩放为`catalog::ThumbRes`与`catalog::Resolution`的比率。
1. 根据`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`将缩放的图像与目标矩形对齐。
1. 将结果裁切到目标矩形。
