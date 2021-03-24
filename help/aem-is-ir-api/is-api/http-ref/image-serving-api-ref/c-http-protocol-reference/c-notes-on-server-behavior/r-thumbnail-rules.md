---
description: 注意这些缩略图规则。
solution: Experience Manager
title: 缩略图规则
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---


# 缩略图规则{#thumbnail-rules}

注意这些缩略图规则。

1. 如果`catalog::ThumbType=Crop`，则（裁剪）图像将缩放到尽可能小的大小，同时仍覆盖整个目标矩形。 如果`catalog::ThumbType=Fit`，则（裁剪）图像将缩放到最大的大小，同时仍将整个图像适合到目标矩形中。 如果`catalog::ThumbType=Texture`，则（裁剪）图像将缩放为`catalog::ThumbRes`与`catalog::Resolution`的比例。
1. 根据`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`将缩放的图像与目标矩形对齐。
1. 将结果裁剪到目标矩形。

