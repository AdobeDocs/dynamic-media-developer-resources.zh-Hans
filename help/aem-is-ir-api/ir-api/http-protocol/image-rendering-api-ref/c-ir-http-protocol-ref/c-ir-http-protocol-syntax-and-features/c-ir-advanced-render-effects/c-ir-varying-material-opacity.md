---
title: 不同材质不透明度
description: 实色和应用于重叠对象的可重复纹理以及小贴片和窗口覆盖材料均支持可变不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 不同材质不透明度{#varying-material-opacity}

实色和应用于重叠对象的可重复纹理以及小贴片和窗口覆盖材料均支持可变不透明度。

不透明度信息可以简单地通过使用带有Alpha通道的RGB图像来提供。 此外，可以使用`opacity=`命令更改整体不透明度(适用于RGB和RGBA图像)。

墙边框还支持RGBA图像，主要支持管芯切割边框。

定义窗口覆盖的[!DNL vnw]文件可以包含不透明度渠道。 它由渲染器与可重复纹理的alpha通道和`opacity=`值组合在一起，以提供用于透明和半透明窗口处理的完整的不透明度效果。
