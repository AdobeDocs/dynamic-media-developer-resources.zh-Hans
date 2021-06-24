---
description: 对于应用于重叠对象的纯色和可重复纹理，以及贴花和窗口覆盖材料，支持可变的不透明度。
solution: Experience Manager
title: 改变材料不透明度
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# 改变材料不透明度{#varying-material-opacity}

对于应用于重叠对象的纯色和可重复纹理，以及贴花和窗口覆盖材料，支持可变的不透明度。

只需使用带有Alpha通道的RGB图像即可提供不透明度信息。 此外，还可以使用`opacity=`命令（对于RGB和RGBA图像）来改变整体不透明度。

墙边界还支持RGBA图像，主要用于支持模切边界。

定义窗口覆盖的[!DNL vnw]文件可以包括不透明度通道，该不透明度通道由渲染器与可重复纹理的Alpha通道和`opacity=`值组合，以提供用于透明和半透明窗口处理的全范围不透明度效果。
