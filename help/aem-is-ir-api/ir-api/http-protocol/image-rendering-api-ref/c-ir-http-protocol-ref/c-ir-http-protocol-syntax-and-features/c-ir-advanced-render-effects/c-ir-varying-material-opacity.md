---
description: 对于应用于重叠对象的纯色和可重复纹理，以及贴面和窗口覆盖材料，支持可变不透明度。
seo-description: 对于应用于重叠对象的纯色和可重复纹理，以及贴面和窗口覆盖材料，支持可变不透明度。
seo-title: 改变材料不透明度
solution: Experience Manager
title: 改变材料不透明度
topic: Scene7 Image Serving - Image Rendering API
uuid: 6af07ea8-44ba-4253-8a26-614725af2f46
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 改变材料不透明度{#varying-material-opacity}

对于应用于重叠对象的纯色和可重复纹理，以及贴面和窗口覆盖材料，支持可变不透明度。

只需将RGB图像与alpha渠道一起使用，即可提供不透明度信息。 此外，可以使用命令(RGB和RGBA图 `opacity=` 像均适用)来改变整体不透明度。

墙边框还支持RGBA图像，主要用于支持模切边框。

定义 [!DNL vnw]`opacity=` 窗口覆盖的文件可以包括不透明度渠道，该不透明度渠道由渲染器与可重复纹理的alpha和值相结合，以提供用于透明和半透明的窗口处理的全范围不透明度效果。
