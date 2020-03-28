---
description: 大多数材料都可以动态着色。
seo-description: 大多数材料都可以动态着色。
seo-title: 着色材料
solution: Experience Manager
title: 着色材料
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 着色材料{#colorizing-materials}

大多数材料都可以动态着色。

着色算法简单，对于色相范围有限的材料图像效果最好。 要对材料着色，渲染器只需减去该值， `bgc=` 然后将该值添加 `color=` 到每个像素值。

如果未指定， `color=` 则禁用着色。 `bgc=` 被橱柜材料忽视；而是使用嵌入到文件中 [!DNL vnc] 的基色值。
