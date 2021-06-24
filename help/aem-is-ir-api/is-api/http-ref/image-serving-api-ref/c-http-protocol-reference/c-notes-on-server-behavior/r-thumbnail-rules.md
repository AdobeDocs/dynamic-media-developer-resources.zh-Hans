---
description: 请注意这些缩略图规则。
solution: Experience Manager
title: 缩略图规则
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: d81dc4ad-dd59-4235-996e-58996f009d88
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# 缩略图规则{#thumbnail-rules}

请注意这些缩略图规则。

1. 如果`catalog::ThumbType=Crop`，则（裁剪的）图像将缩放到尽可能小的大小，同时仍覆盖整个目标直角。 如果`catalog::ThumbType=Fit`，则（裁剪的）图像会缩放到尽可能大的大小，同时仍会将整个图像拟合到目标方向中。 如果为`catalog::ThumbType=Texture`，则（裁剪的）图像会缩放为`catalog::ThumbRes`与`catalog::Resolution`的比值。
1. 根据`attribute::ThumbHorizAlign`和`attribute::ThumbVertAlign`将缩放的图像与目标方向对齐。
1. 将结果裁剪到目标方向。
