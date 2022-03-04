---
title: 改变材料不透明度
description: 对于应用于重叠对象的纯色和可重复纹理，以及贴花和窗口覆盖材料，支持可变的不透明度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# 改变材料不透明度{#varying-material-opacity}

对于应用于重叠对象的纯色和可重复纹理，以及贴花和窗口覆盖材料，支持可变的不透明度。

通过使用带有Alpha通道的RGB图像，可以简单地提供不透明度信息。 此外，整体不透明度可随 `opacity=` 命令(对于RGB和RGBA图像)。

墙边界还支持RGBA图像，主要用于支持模切边界。

的 [!DNL vnw] 定义窗口覆盖的文件可以包括不透明度通道。 它由渲染器与可重复纹理的Alpha通道和 `opacity=` 值，为透明和半透明的窗口处理提供全方位的不透明效果。
